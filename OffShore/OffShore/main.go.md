445    WS03             package main
SMB         172.16.2.102    445    WS03             import (
SMB         172.16.2.102    445    WS03             "fmt"
SMB         172.16.2.102    445    WS03             "os/exec"
SMB         172.16.2.102    445    WS03             "strings"
SMB         172.16.2.102    445    WS03             "net/http"
SMB         172.16.2.102    445    WS03             
SMB         172.16.2.102    445    WS03             "github.com/auth0/go-jwt-middleware"
SMB         172.16.2.102    445    WS03             "github.com/dgrijalva/jwt-go"
SMB         172.16.2.102    445    WS03             )
SMB         172.16.2.102    445    WS03             
SMB         172.16.2.102    445    WS03             var secret = []byte("PSmu3dR2wMZQvNge")
SMB         172.16.2.102    445    WS03             
SMB         172.16.2.102    445    WS03             var RunCmd = http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
SMB         172.16.2.102    445    WS03             // Extract token from header
SMB         172.16.2.102    445    WS03             var tokenstring string
SMB         172.16.2.102    445    WS03             tokens, ok := r.Header["Authorization"]
SMB         172.16.2.102    445    WS03             if ok && len(tokens) <= 2 {
SMB         172.16.2.102    445    WS03             tokenstring = tokens[0]
SMB         172.16.2.102    445    WS03             tokenstring = strings.TrimPrefix(tokenstring, "Bearer ")
SMB         172.16.2.102    445    WS03             }
SMB         172.16.2.102    445    WS03             
SMB         172.16.2.102    445    WS03             // Extract cmd
SMB         172.16.2.102    445    WS03             token, _ := jwt.Parse(tokenstring, func(token *jwt.Token) (interface{}, error) {
SMB         172.16.2.102    445    WS03             return secret, nil
SMB         172.16.2.102    445    WS03             })
SMB         172.16.2.102    445    WS03             cmd := token.Claims.(jwt.MapClaims)["cmd"].(string)
SMB         172.16.2.102    445    WS03             
SMB         172.16.2.102    445    WS03             // Execute command
SMB         172.16.2.102    445    WS03             // BUG: This only will work on linux, this was a hack to easily allow arguments to be sent.
SMB         172.16.2.102    445    WS03             //      Unfortunately, it broke the code on Windows.  Either need to look into parsing
SMB         172.16.2.102    445    WS03             //      arguments, or simply create an if/then to check for OS.
SMB         172.16.2.102    445    WS03             // No command should contain a space.
SMB         172.16.2.102    445    WS03             if strings.Contains(cmd, " ") {
SMB         172.16.2.102    445    WS03             fmt.Fprintf(w, "Hacker Detected!")
SMB         172.16.2.102    445    WS03             } else {
SMB         172.16.2.102    445    WS03             // Execute command
SMB         172.16.2.102    445    WS03             output, _ := exec.Command("sh","-c", cmd).Output()
SMB         172.16.2.102    445    WS03             fmt.Fprintf(w, "%s", output)
SMB         172.16.2.102    445    WS03             }
SMB         172.16.2.102    445    WS03             })
SMB         172.16.2.102    445    WS03             
SMB         172.16.2.102    445    WS03             func main() {
SMB         172.16.2.102    445    WS03             jwtMiddleware := jwtmiddleware.New(jwtmiddleware.Options{
SMB         172.16.2.102    445    WS03             ValidationKeyGetter: func(token *jwt.Token) (interface{}, error) {
SMB         172.16.2.102    445    WS03             return secret, nil
SMB         172.16.2.102    445    WS03             },
SMB         172.16.2.102    445    WS03             SigningMethod: jwt.SigningMethodHS256,
SMB         172.16.2.102    445    WS03             })
SMB         172.16.2.102    445    WS03             
SMB         172.16.2.102    445    WS03             app := jwtMiddleware.Handler(RunCmd)
SMB         172.16.2.102    445    WS03             http.ListenAndServe("0.0.0.0:3000", app)
SMB         172.16.2.102    445    WS03             }

$ curl -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyLCJpc3MiOiJnby1qd3QtbWlkZGxld2FyZS1leGFtcGxlIiwiYXVkIjoiZ28tand0LW1pZGRsZXdhcmUtZXhhbXBsZSJ9.xcnkyPYu_b3qm2yeYuEgr5R5M5t4pN9s04U1ya53-KM" localhost:3000