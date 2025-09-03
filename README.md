# xxe-injection-payload

In this section, we'll explain what XML external entity injection is, describe some common examples, explain how to find and exploit various kinds of XXE injection, and summarize how to prevent XXE injection attacks.

What is XML external entity injection?
XML external entity injection (also known as XXE) is a web security vulnerability that allows an attacker to interfere with an application's processing of XML data. It often allows an attacker to view files on the application server filesystem, and to interact with any backend or external systems that the application itself can access.

In some situations, an attacker can escalate an XXE attack to compromise the underlying server or other backend infrastructure, by leveraging the XXE vulnerability to perform server-side request forgery (SSRF) attacks.



| XXE Attack Type                                   | Description                                                                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Exploiting XXE to Retrieve Files                  | An external entity is defined containing the contents of a file, which is then returned in the application's response. |
| Exploiting XXE to Perform SSRF Attacks            | An external entity is defined based on a URL to a back-end system.                            |
| Exploiting Blind XXE to Exfiltrate Data Out-of-Band | Sensitive data is transmitted from the application server to a system controlled by the attacker. |
| Exploiting Blind XXE to Retrieve Data Via Error Messages | The attacker triggers a parsing error message that contains sensitive data.                     |
