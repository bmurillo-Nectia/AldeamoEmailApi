// Configuración #1
{
  "to": [
    {
      "email": "example@exampledomain.com"  -- Campo:NecTools__Field_To__c (Campo del correo del objeto) Ej: Email__c
    }
  ],
  "options": {
    "cc": [
      {
        "email": "cc@exampledomain.com"    -- Campo:NecTools__cc__c (Correos de copia separados por coma) Ej: example@gmail.com,example1@gmail.com
      }
    ],
    "bcc": [
      {
        "email": "bcc@exampledomain.com"   -- Campo:NecTools__bcc__c (Correos de copia oculta separados por coma) Ej: example@gmail.com,example1@gmail.com
      }
    ]
  },
  "from": {
    "email": "sender@yourdomain.com",      -- Campo:NecTools__Correo_remitente__c (Correo Remitente) Ej: example@dominioregistrado.com
    "name": "John Doe"                     -- Campo:NecTools__Nombre_remitente__c (Nombre Remitente) Ej: John Fast
  },
  "replyTo": {
    "email": "sender@yourdomain.com",
    "name": "John Doe"
  },
  "subject": "Hello World",                -- Campo:NecTools__Asunto__c (Asunto) Ej: Nueva linea de venta
  "body": "<h1>Hello World</h1>"           -- Campo:NecTools__Cuerpo__c (HTML) Ej: <h1>Hello World</h1>
}

// Nota: Si desea enviar archivo adjunto por URL, utilice el campo "NecTools__Adjunto_1__c" y sus concecutivos, en caso de querer enviar adjuntos desde salesforce, suba el archivo de la siguiente manera: https://help.salesforce.com/articleView?id=admin_files_asset_files_create.htm&type=5, copie y pegue el nombre del archivo en el campo "NecTools__filename_1__c" o sus concecutivos. recuerde que si elección es el envío por URL deje en blanco el campo "NecTools__filename_1__c" y si su envio es por nombre deje en blanco el campo "NecTools__Adjunto_1__c"

{
  "attachments": [{
    	"path":"https://imagen.gif"          -- Campo: (NecTools__Adjunto_1__c) o (NecTools__filename_1__c)
  	},
  	{
      "filename":"pdf1.pdf"
      "path":"data:application/pdf;base64,iVBORw0KGgoAAAANSUhEUgAAB9AAA="	 -- Campo: (NecTools__Adjunto_1__c) o (NecTools__filename_1__c)
  	}]
}
