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
# <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="3a885-102">Scénario de persistance du recordset au format XML</span><span class="sxs-lookup"><span data-stu-id="3a885-102">XML Recordset persistence scenario</span></span>

<span data-ttu-id="3a885-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a885-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a885-104">Ce scénario consiste à créer une application ASP (Active Server Pages) enregistrant directement le contenu d'un objet **Recordset** dans l'objet **Response** ASP.</span><span class="sxs-lookup"><span data-stu-id="3a885-104">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a **Recordset** object directly to the ASP **Response** object.</span></span>

> [!NOTE]
> <span data-ttu-id="3a885-105">[!REMARQUE] Pour les besoins de ce scénario, Internet Information Server 5.0 (IIS) ou une version ultérieure doit être installé sur votre serveur.</span><span class="sxs-lookup"><span data-stu-id="3a885-105">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</span></span>

<span data-ttu-id="3a885-106">L'objet **Recordset** retourné est affiché dans Internet Explorer à l'aide d'un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="3a885-106">The returned **Recordset** is displayed in Internet Explorer using an [RDS.DataControl](datacontrol-object-rds.md).</span></span>

<span data-ttu-id="3a885-107">Pour créer ce scénario, il est nécessaire d'exécuter les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="3a885-107">The following steps are necessary to create this scenario:</span></span>

1.  <span data-ttu-id="3a885-108">Configurer l'application</span><span class="sxs-lookup"><span data-stu-id="3a885-108">Set up the application.</span></span>
2.  <span data-ttu-id="3a885-109">Obtenir les données</span><span class="sxs-lookup"><span data-stu-id="3a885-109">Get the data.</span></span>
3.  <span data-ttu-id="3a885-110">Envoyer les données</span><span class="sxs-lookup"><span data-stu-id="3a885-110">Send the data.</span></span>
4.  <span data-ttu-id="3a885-111">Recevoir et afficher les données</span><span class="sxs-lookup"><span data-stu-id="3a885-111">Receive and display the data.</span></span>

## <a name="step-1-set-up-the-application"></a><span data-ttu-id="3a885-112">Étape 1 : Configurer l’application</span><span class="sxs-lookup"><span data-stu-id="3a885-112">Step 1: Set up the application</span></span>

1. <span data-ttu-id="3a885-113">Créez un répertoire virtuel IIS nommé **XMLPersist** avec des autorisations de script.</span><span class="sxs-lookup"><span data-stu-id="3a885-113">Create an IIS virtual directory named **XMLPersist** with script permissions.</span></span> 

2. <span data-ttu-id="3a885-114">Créez deux nouveaux fichiers texte dans le dossier vers lequel pointe le répertoire **virtuel,** l’un nommé **XMLResponse.asp** et l’autre nomméDefault.htm.</span><span class="sxs-lookup"><span data-stu-id="3a885-114">Create two new text files in the folder to which the virtual directory points, one named **XMLResponse.asp**, and the other named **Default.htm**.</span></span>


## <a name="step-2-get-the-data"></a><span data-ttu-id="3a885-115">Étape 2 : Obtenir les données</span><span class="sxs-lookup"><span data-stu-id="3a885-115">Step 2: Get the data</span></span>

<span data-ttu-id="3a885-116">Cette étape consiste à écrire le code permettant d'ouvrir un objet **Recordset** ADO et de préparer son envoi au client.</span><span class="sxs-lookup"><span data-stu-id="3a885-116">In this step, you will write the code to open an ADO **Recordset** and prepare to send it to the client.</span></span> 

1. <span data-ttu-id="3a885-117">Ouvrez le fichier XMLResponse.asp dans un éditeur de texte, tel que le Bloc-notes de Windows, puis insérez-y le code suivant :</span><span class="sxs-lookup"><span data-stu-id="3a885-117">Open the file XMLResponse.asp with a text editor, such as Windows Notepad, and insert the following code:</span></span>

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

2. <span data-ttu-id="3a885-118">N’oubliez pas de modifier la valeur du paramètre De source de données dans strCon en nom de votre ordinateur Microsoft SQL Server données.</span><span class="sxs-lookup"><span data-stu-id="3a885-118">Be sure to change the value of the Data Source parameter in strCon to the name of your Microsoft SQL Server computer.</span></span>

3. <span data-ttu-id="3a885-119">Gardez le fichier ouvert et passez à l'étape suivante.</span><span class="sxs-lookup"><span data-stu-id="3a885-119">Keep the file open and go on to the next step.</span></span>

## <a name="step-3-send-the-data"></a><span data-ttu-id="3a885-120">Étape 3 : Envoyer les données</span><span class="sxs-lookup"><span data-stu-id="3a885-120">Step 3: Send the data</span></span>

<span data-ttu-id="3a885-121">À présent que vous disposez d'un objet **Recordset**, vous devez l'envoyer au client en l'enregistrant en tant que fichier XML dans l'objet **Response** ASP.</span><span class="sxs-lookup"><span data-stu-id="3a885-121">Now that you have a **Recordset**, you need to send it to the client by saving it as XML to the ASP **Response** object.</span></span> 

1. <span data-ttu-id="3a885-122">Ajoutez le code suivant au bas de XMLResponse.asp :</span><span class="sxs-lookup"><span data-stu-id="3a885-122">Add the following code to the bottom of XMLResponse.asp:</span></span>

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

   <span data-ttu-id="3a885-123">Notez que l’objet de **réponse** ASP est spécifié comme destination de la méthode **Recordset** [Save.](save-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="3a885-123">Notice that the ASP **Response** object is specified as the destination for the **Recordset** [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="3a885-124">La destination de la méthode **Save** peut représenter n'importe quel objet prenant en charge l'interface **IStream**, par exemple, un objet [Stream](stream-object-ado.md) ADO ou un nom de fichier incluant le chemin d'accès complet à l'emplacement au niveau duquel est enregistré l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3a885-124">The destination of the **Save** method can be any object that supports the **IStream** interface, such as an ADO [Stream](stream-object-ado.md) object, or a file name that includes the complete path to which the **Recordset** is to be saved.</span></span>

2. <span data-ttu-id="3a885-125">Enregistrez et fermez XMLResponse.asp avant de passer à l'étape suivante.</span><span class="sxs-lookup"><span data-stu-id="3a885-125">Save and close XMLResponse.asp before going to the next step.</span></span> <span data-ttu-id="3a885-126">Copiez également le fichier adovbs.inc à partir du dossier C: Program Files Common Files System Ado dans le dossier où vous avez le fichier \\ \\ \\ \\ XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="3a885-126">Also copy the adovbs.inc file from C:\\Program Files\\Common Files\\System\\Ado folder to the same folder where you have the XMLResponse.asp file.</span></span>

## <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="3a885-127">Étape 4 : Recevoir et afficher les données</span><span class="sxs-lookup"><span data-stu-id="3a885-127">Step 4: Receive and display the data</span></span>

<span data-ttu-id="3a885-128">Dans cette étape, vous allez créer un fichier HTML avec un [rdS incorporé. Objet DataControl](datacontrol-object-rds.md) qui pointe vers le fichier XMLResponse.asp pour obtenir le **recordset**.</span><span class="sxs-lookup"><span data-stu-id="3a885-128">In this step, you will create an HTML file with an embedded [RDS.DataControl](datacontrol-object-rds.md) object that points at the XMLResponse.asp file to get the **Recordset**.</span></span> 

1. <span data-ttu-id="3a885-129">Ouvrez default.htm avec un éditeur de texte, tel que le Bloc-notes Windows, et ajoutez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="3a885-129">Open default.htm with a text editor, such as Windows Notepad, and add the following code.</span></span> <span data-ttu-id="3a885-130">Remplacez « sqlserver » dans l'URL par le nom de votre serveur.</span><span class="sxs-lookup"><span data-stu-id="3a885-130">Replace "sqlserver" in the URL with the name of your server computer.</span></span>

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

2. <span data-ttu-id="3a885-131">Fermez le fichier default.htm et enregistrez-le dans le dossier où vous avez enregistré XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="3a885-131">Close the default.htm file and save it to the same folder where you saved XMLResponse.asp.</span></span> 

3. <span data-ttu-id="3a885-132">À l’aide d’Internet Explorer 4.0 ou d’une ultérieure, ouvrez l’URL `https://<sqlserver>/XMLPersist/default.htm` et observez les résultats.</span><span class="sxs-lookup"><span data-stu-id="3a885-132">Using Internet Explorer 4.0 or later, open the URL `https://<sqlserver>/XMLPersist/default.htm` and observe the results.</span></span> <span data-ttu-id="3a885-133">Les données s'affichent dans un tableau DHTML lié.</span><span class="sxs-lookup"><span data-stu-id="3a885-133">The data is displayed in a bound DHTML table.</span></span> 

4. <span data-ttu-id="3a885-134">Ouvrez maintenant l’URL `https://<sqlserver>/XMLPersist/XMLResponse.asp` et observez les résultats.</span><span class="sxs-lookup"><span data-stu-id="3a885-134">Now open the URL `https://<sqlserver>/XMLPersist/XMLResponse.asp` and observe the results.</span></span> <span data-ttu-id="3a885-135">Le fichier XML s'affiche.</span><span class="sxs-lookup"><span data-stu-id="3a885-135">The XML is displayed.</span></span>




