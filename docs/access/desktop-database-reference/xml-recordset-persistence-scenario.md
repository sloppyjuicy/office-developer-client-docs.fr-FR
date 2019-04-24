---
title: Scénario de persistance du recordset au format XML
TOCTitle: XML Recordset persistence scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5bae48f3e9b2b5c3967b955c41ba01c634546164
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302592"
---
# <a name="xml-recordset-persistence-scenario"></a>Scénario de persistance du recordset au format XML

**S’applique à** : Access 2013, Office 2013

Ce scénario consiste à créer une application ASP (Active Server Pages) enregistrant directement le contenu d'un objet **Recordset** dans l'objet **Response** ASP.

> [!NOTE]
> [!REMARQUE] Pour les besoins de ce scénario, Internet Information Server 5.0 (IIS) ou une version ultérieure doit être installé sur votre serveur.

L'objet **Recordset** retourné est affiché dans Internet Explorer à l'aide d'un objet [RDS.DataControl](datacontrol-object-rds.md).

Pour créer ce scénario, il est nécessaire d'exécuter les étapes suivantes :

1.  Configurer l'application
2.  Obtenir les données
3.  Envoyer les données
4.  Recevoir et afficher les données

## <a name="step-1-set-up-the-application"></a>Étape 1: configurer l'application

1. Créez un répertoire virtuel IIS nommé **XMLPersist** avec des autorisations de script. 

2. Créez deux nouveaux fichiers texte dans le dossier vers lequel pointe le répertoire virtuel, un nommé **XMLResponse. asp**et l'autre nommé **default. htm**.


## <a name="step-2-get-the-data"></a>Étape 2: obtenir les données

Cette étape consiste à écrire le code permettant d'ouvrir un objet **Recordset** ADO et de préparer son envoi au client. 

1. Ouvrez le fichier XMLResponse.asp dans un éditeur de texte, tel que le Bloc-notes de Windows, puis insérez-y le code suivant :

   ```vb 
        
        <%@ language="VBScript" %> 
        
        <!-- #include file='adovbs.inc' --> 
        
        <% 
        Dim strSQL, strCon 
        Dim adoRec  
        Dim adoCon  
        Dim xmlDoc  
        
        ' You will need to change "slqServer" below to the name of the SQL  
        ' server machine to which you want to connect. 
        strCon = "Provider=sqloledb;Data Source=sqlServer;Initial Catalog=Pubs;Integrated Security=SSPI;" 
        Set adoCon = server.createObject("ADODB.Connection") 
        adoCon.Open strCon 
        
        strSQL = "SELECT Title, Price FROM Titles ORDER BY Price" 
        Set adoRec = Server.CreateObject("ADODB.Recordset") 
        adoRec.Open strSQL, adoCon, adOpenStatic, adLockOptimistic, adCmdText 
   ```

2. Veillez à modifier la valeur du paramètre source de données dans strCon sur le nom de votre ordinateur Microsoft SQL Server.

3. Gardez le fichier ouvert et passez à l'étape suivante.

## <a name="step-3-send-the-data"></a>Étape 3: envoyer les données

À présent que vous disposez d'un objet **Recordset**, vous devez l'envoyer au client en l'enregistrant en tant que fichier XML dans l'objet **Response** ASP. 

1. Ajoutez le code suivant au bas de XMLResponse.asp :

   ```vb 
    
    Response.ContentType = "text/xml" 
    Response.Expires = 0 
    Response.Buffer = False 
    
    
    Response.Write "<?xml version='1.0'?>" & vbNewLine 
    adoRec.save Response, adPersistXML 
    adoRec.Close 
    Set adoRec=Nothing 
    %> 
   ```

   Notez que l'objet de **réponse** ASP est spécifié comme destination de la méthode [Save](save-method-ado.md) de l'objet **Recordset** . La destination de la méthode **Save** peut représenter n'importe quel objet prenant en charge l'interface **IStream**, par exemple, un objet [Stream](stream-object-ado.md) ADO ou un nom de fichier incluant le chemin d'accès complet à l'emplacement au niveau duquel est enregistré l'objet **Recordset**.

2. Enregistrez et fermez XMLResponse.asp avant de passer à l'étape suivante. Copiez également le fichier adovbs. Inc du dossier\\ADO du\\système\\de\\fichiers communs C: Program Files dans le dossier où se trouve le fichier XMLResponse. asp.

## <a name="step-4-receive-and-display-the-data"></a>Étape 4: recevoir et afficher les données

Dans cette étape, vous allez créer un fichier HTML avec un [objet RDS incorporé. DataControl](datacontrol-object-rds.md) qui pointe sur le fichier XMLResponse. asp pour obtenir l'objet **Recordset**. 

1. Ouvrez default. htm avec un éditeur de texte, tel que le bloc-notes Windows, et ajoutez le code suivant. Remplacez « sqlserver » dans l'URL par le nom de votre serveur.

   ```html 
    
    <HTML> 
    <HEAD><TITLE>ADO Recordset Persistence Sample</TITLE></HEAD> 
    <BODY> 
    
    <TABLE DATASRC="#RDC1" border="1"> 
    <TR> 
    <TD><SPAN DATAFLD="title"></SPAN></TD> 
    <TD><SPAN DATAFLD="price"></SPAN></TD> 
    </TR> 
    </TABLE> 

    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="RDC1"> 
    <PARAM NAME="URL" VALUE="XMLResponse.asp"> 
    </OBJECT> 
    
    </BODY> 
    </HTML> 
   ```

2. Fermez le fichier default.htm et enregistrez-le dans le dossier où vous avez enregistré XMLResponse.asp. 

3. À l'aide d'Internet Explorer 4,0 ou version ultérieure `https://<sqlserver>/XMLPersist/default.htm` , ouvrez l'URL et observez les résultats. Les données s'affichent dans un tableau DHTML lié. 

4. Ouvrez à présent l' `https://<sqlserver>/XMLPersist/XMLResponse.asp` URL et observez les résultats. Le fichier XML s'affiche.




