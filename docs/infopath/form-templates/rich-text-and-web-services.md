---
title: Texte enrichi et services Web
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 53fddc3f-e9d9-db76-6b84-11befdb23fb0
description: "Microsoft InfoPath prend en charge la liaison d'un contrôle Zone de texte mis en forme dans un formulaire à un élément XML reçu à partir d'un service Web, ainsi que l'envoi de données à partir d'un tel contrôle vers un élément XML via un service Web. L'élément doit respecter le format XHTML (Extensible HyperText Markup Language). Par exemple, le schéma d'un élément nommé MyRichTextElement qui contient du texte enrichi aurait la définition de schéma XML suivante :"
ms.openlocfilehash: 07a7a3dbc0f054160adce54e316b01797feacd8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782456"
---
# <a name="rich-text-and-web-services"></a><span data-ttu-id="afb64-105">Texte enrichi et services Web</span><span class="sxs-lookup"><span data-stu-id="afb64-105">Rich Text and Web Services</span></span>

<span data-ttu-id="afb64-p102">Microsoft InfoPath prend en charge la liaison d'un contrôle **Zone de texte mis en forme** dans un formulaire à un élément XML reçu à partir d'un service Web, ainsi que l'envoi de données à partir d'un tel contrôle vers un élément XML via un service Web. L'élément doit respecter le format XHTML (Extensible HyperText Markup Language). Par exemple, le schéma d'un élément nommé  `MyRichTextElement` qui contient du texte enrichi aurait la définition de schéma XML suivante :</span><span class="sxs-lookup"><span data-stu-id="afb64-p102">Microsoft InfoPath supports binding a **Rich Text Box** control in a form to an XML element that is received from a Web service, and submitting data from a rich text box control to an XML element through a Web service. The element must adhere to the Extensible HyperText Markup Language (XHTML) format. For example, the schema for an element named  `MyRichTextElement` that contains rich text would have the following XML schema definition:</span></span> 
  
```XML
<xsd:element name="MyRichTextElement"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="http://www.w3.org/1999/xhtml" processContents="lax" 
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element>
```

<span data-ttu-id="afb64-p103">Pour pouvoir lier un contrôle **Zone de texte mis en forme** à l'élément XHTML, cet élément doit être incorporé dans un nœud wrapper ; ce nœud peut appartenir à un espace de noms arbitraire et ressembler à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="afb64-p103">Before a **Rich Text Box** control can be bound with the XHTML element, the element should be wrapped with a wrapper node; this wrapper node can belong to any arbitrary namespace. The wrapper node can look like this:</span></span> 
  
```xml
<xhtmlNode xmlns="http:// someNamespace"> 
    <div xmlns="http://www.w3.org/1999/xhtml">Your rich text here</div> 
</xhtmlNode>
```

<span data-ttu-id="afb64-p104">Cette rubrique donne une vue d'ensemble du processus de création d'un service Web qui peut envoyer et recevoir du code XHTML. Elle présente également comment utiliser InfoPath pour effectuer la liaison aux paramètres du service Web. Mais, elle ne donne pas la procédure détaillée pour créer un tel service Web. Il est supposé que vous avez des connaissances sur l'utilisation des services Web.</span><span class="sxs-lookup"><span data-stu-id="afb64-p104">This topic outlines the process of creating a Web service that can send and receive XHTML, and how to use InfoPath to bind to the Web service parameters. This topic does not provide detailed instructions on how to create such a Web service. It is assumed that you already have some familiarity with working with Web services.</span></span>
  
## <a name="how-to-design-a-web-service-to-receive-and-send-xhtml"></a><span data-ttu-id="afb64-114">Comment concevoir un service Web pour recevoir et envoyer du code XHTML</span><span class="sxs-lookup"><span data-stu-id="afb64-114">How to Design a Web Service to Receive and Send XHTML</span></span>

<span data-ttu-id="afb64-p105">Le service Web en exemple stocke les données XHTML qu'il envoie et reçoit dans un fichier XML sur le serveur. Ce fichier, nommé out.xml, agit comme une source de données qui stocke les données XHTML. Deux méthodes Web qui seront présentées permettent d'interfacer une application cliente avec la source de données XHTML :  `getXhtml` et  `setXhtml`. La méthode  `getXhtml` de service Web retourne un **XmlNode** qui contient le code XHTML qui peut être lié à un contrôle de zone de texte enrichi InfoPath. La méthode  `setXhtml` de service Web accepte un **XmlNode** en tant que données à stocker dans le fichier out.xml.</span><span class="sxs-lookup"><span data-stu-id="afb64-p105">The example Web service stores the XHTML data that it sends and receives in an XML file on the server. This file that is named out.xml, acts as a data source that stores the XHTML data. There are two Web methods that will be exposed to allow a client application to interface with the XHTML data source:  `getXhtml` and  `setXhtml`. The  `getXhtml` Web Service method returns an **XmlNode** that contains the XHTML that can be bound to an InfoPath rich text box control. The  `setXhtml` Web Service method accepts an **XmlNode** as the data to store in the out.xml file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="afb64-120">[!REMARQUE] Ces méthodes Web requièrent des déclarations **using** pour faire référence aux espaces de noms **System.IO** et **System.Xml**.</span><span class="sxs-lookup"><span data-stu-id="afb64-120">These Web methods require **using** statements that reference the **System.IO** and **System.Xml** namespaces.</span></span> 
  
<span data-ttu-id="afb64-121">La méthode  `getXhtml` de service Web essaie de charger les données XML à renvoyer à partir du fichier out.xml situé dans le dossier Data sur le lecteur C. Si elle échoue, parce que le fichier est introuvable ou ne contient pas du code XML valide, elle retourne un élément HTML **DIV** vide qui fait référence à l'espace de noms XHTML.</span><span class="sxs-lookup"><span data-stu-id="afb64-121">The  `getXhtml` Web Service method attempts to load the XML data to be returned from the out.xml file in the Data folder on drive C. If it fails, because the file is not found, or does not contain valid XML, the method will return an empty **DIV** HTML element that references the XHTML namespace.</span></span> 
  
```cs
[WebMethod]
public XmlNode getXhtml()  
{  
            // This is the returned XmlDocument upon Query from InfoPath 
            XmlDocument document = new XmlDocument(); 
 
            // Create a wrapping node with the name of the rich text field. 
            // The "http://someNameSpace" can be any arbitrary namespace 
            XmlNode richNode = document.CreateNode 
                        (XmlNodeType.Element, "MyRichTextElement", "http://someNameSpace"); 
 
            // Temporary XmlDocument 
            XmlDocument tempDocument = new XmlDocument(); 
            try 
            { 
                // Read the saved rich text data from the local machine 
                tempDocument.Load(@"c:\Data\out.xml"); 
            } 
            catch (XmlException) 
            { 
                // If the file does not exist or content is not valid XML 
                tempDocument.LoadXml("<div xmlns=\"http://www.w3.org/1999/xhtml\"></div>"); 
            } 
 
            // Add the file content to the xml 
            richNode.AppendChild 
                        (document.ImportNode(tempDocument.DocumentElement, true)); 
 
            return richNode; 
}  

```

<span data-ttu-id="afb64-p106">La méthode  `setXhtml` de service Web accepte le code XHTML d'un contrôle **Zone de texte mis en forme** sur un formulaire InfoPath. Comme les services Web ne prennent pas en charge de liste de nœuds, lorsqu'un champ de texte enrichi contenant plusieurs lignes est envoyé à un service Web, ce dernier n'accepte que la première ligne et ignore le reste.</span><span class="sxs-lookup"><span data-stu-id="afb64-p106">The  `setXhtml` Web Service method accepts XHTML from a **Rich Text Box** control on an InfoPath form. Because Web services do not support a node list, when a rich text field that contains multiple lines is sent to a Web service, the Web service only accepts the first line and ignores the rest.</span></span> 
  
<span data-ttu-id="afb64-p107">La méthode  `setXhtml` en exemple suppose qu'elle recevra un nœud XML de niveau supérieur, qui dans la plupart des cas sera incorporé dans un élément **DIV**. Si le code XML reçu ne contient pas d'élément englobant, par exemple lorsque le texte à l'intérieur du contrôle **Zone de texte mis en forme** n'est pas formaté, cette méthode le détectera en vérifiant si la propriété **NodeType** indique que le code XML transmis est un nœud de texte, auquel cas elle crée un élément **DIV** et copie le contenu du nœud de texte dans l'élément **DIV** afin que le **DIV**contienne un nœud de texte enfant avec le texte qui avait été envoyé au service Web. Le code XML reçu par cette méthode est écrit dans le fichier out.xml situé dans le dossier Data sur le lecteur C.</span><span class="sxs-lookup"><span data-stu-id="afb64-p107">The sample  `setXhtml` method assumes that it will receive a top-level XML node, which in most cases will be wrapped in a **DIV** element. If the XML received does not contain a wrapping element, for example when text within the **Rich Text Box** control has no formatting, this method will detect this by checking whether the **NodeType** property indicates that the XML passed in is a text node. If the XML is a text node, the method creates a **DIV** element and copies the text node contents to the **DIV** so that the **DIV** contains a text node child with the text that was sent to the Web service. The XML received by this method is written to the out.xml file in the Data folder on the drive C.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="afb64-p108">[!REMARQUE] La méthode  `setXhtml` en exemple a été conçue pour accepter des données XHTML de toutes tailles. Dans la pratique, vérifiez systématiquement la quantité de données envoyées et fixez une limite supérieure pour celle-ci.</span><span class="sxs-lookup"><span data-stu-id="afb64-p108">The sample  `setXhtml` method was written to accept XHTML data of any size. In actual practice, you should always check to see how much data is being submitted and set an upper limit for how much data that can be submitted.</span></span> 
  
```cs
[WebMethod]  
public void setXhtml(XmlNode xn)  
{  
            XmlDocument document = new XmlDocument(); 
 
            if (xn == null) 
            { 
                // If nothing was submitted or the rich text field is empty, 
                // create a DIV that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "http://www.w3.org/1999/xhtml"); 
                // Copy the node to our own XmlDocument 
                document.AppendChild(div); 
            } 
            if (xn.NodeType == XmlNodeType.Text) 
            { 
                // If plain text is passed in, wrap it in a DIV 
                // that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "http://www.w3.org/1999/xhtml"); 
                // Copy the text to the DIV. 
                div.AppendChild(document.ImportNode(xn, true)); 
                // Copy the node to our own XmlDocument 
                document.AppendChild(div); 
            } 
            else 
            { 
                // Copy the node to our own XmlDocument 
                document.AppendChild(document.ImportNode(xn, true)); 
            } 
 
            // Save the file to the local machine 
            document.Save(@"c:\Data\out.xml"); 
}  

```

## <a name="how-to-create-an-infopath-form-that-exchanges-data-with-the-sample-web-service"></a><span data-ttu-id="afb64-130">Comment créer un formulaire InfoPath qui échange des données avec le service Web en exemple</span><span class="sxs-lookup"><span data-stu-id="afb64-130">How to Create an InfoPath Form That Exchanges Data with the Sample Web Service</span></span>

<span data-ttu-id="afb64-131">Pour créer un formulaire afin de tester le service Web en exemple, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="afb64-131">Perform the following steps to create a form to test the sample Web service.</span></span>
  
### <a name="to-create-a-form-that-connects-to-the-sample-web-service"></a><span data-ttu-id="afb64-132">Pour créer un formulaire qui se connecte au service Web en exemple</span><span class="sxs-lookup"><span data-stu-id="afb64-132">To create a form that connects to the sample Web service</span></span>

1. <span data-ttu-id="afb64-133">Ouvrez le concepteur de formulaires InfoPath.</span><span class="sxs-lookup"><span data-stu-id="afb64-133">Open the InfoPath form designer.</span></span>
    
2. <span data-ttu-id="afb64-134">Sur l'onglet **Nouveau**, double-cliquez sur **Service Web** sous **Modèles de formulaires avancés**.</span><span class="sxs-lookup"><span data-stu-id="afb64-134">On the **New** tab, double-click **Web Service** under **Advanced Form Templates**.</span></span>
    
3. <span data-ttu-id="afb64-135">Dans la boîte de dialogue **Assistant Connexion de données**, cliquez sur **Réception des données**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="afb64-135">In the **Data Connection Wizard** dialog box, select **Receive data**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="afb64-136">Tapez l'adresse du service Web qui contient les méthodes du service Web en exemple, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="afb64-136">Type the address of the Web service that contains the sample Web service methods, and then click **Next**.</span></span> 
    
5. <span data-ttu-id="afb64-137">Pour la méthode de réception, sélectionnez **getXhtml** comme opération, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="afb64-137">For the receive method, select **getXhtml** as the operation, and then click **Next**.</span></span>
    
6. <span data-ttu-id="afb64-138">La méthode de service Web **getXHTML** ne prenant aucun paramètre en charge, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="afb64-138">The **getXHTML** Web service method takes no parameters, so click **Next**.</span></span>
    
7. <span data-ttu-id="afb64-139">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="afb64-139">Click **Finish**.</span></span>
    
8. <span data-ttu-id="afb64-140">Sur l'onglet **Données**, dans le groupe **Actions d'envoi**, cliquez sur **À d'autres emplacements**, puis sur **Service Web** afin d'utiliser le même service Web pour l'envoi des données.</span><span class="sxs-lookup"><span data-stu-id="afb64-140">On the **Data** tab, in the **Submit Actions** group click **To Other Locations**, and then click **Web Service** to use the same Web service to the submit data.</span></span> 
    
9. <span data-ttu-id="afb64-141">Tapez l'adresse du service Web qui contient les méthodes du service Web en exemple, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="afb64-141">Type the address of the Web service that contains the sample Web service methods, and then click **Next**.</span></span>
    
10. <span data-ttu-id="afb64-142">Pour la méthode d'envoi, sélectionnez **setXhtml** comme opération, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="afb64-142">For the submit method, select **setXhtml** as the operation, and then click **Next**.</span></span>
    
11. <span data-ttu-id="afb64-143">Cliquez sur **Modifier**, développez le dossier **dataFields**, puis le dossier **s0:getXhtmlResponse**, puis le dossier **getXhtmlResult**, sélectionnez l'élément **MyRichTextElement**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="afb64-143">Click **Modify**, expand the **dataFields** folder, expand the **s0:getXhtmlResponse** folder, expand the **getXhtmlResult** folder, select the **MyRichTextElement** element, and then click **Next**.</span></span>
    
12. <span data-ttu-id="afb64-144">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="afb64-144">Click **Finish**.</span></span>
    
13. <span data-ttu-id="afb64-145">Dans le volet Office **Champs**, développez le dossier **dataFields**.</span><span class="sxs-lookup"><span data-stu-id="afb64-145">In the **Fields** task pane, expand the **dataFields** folder.</span></span> 
    
14. <span data-ttu-id="afb64-p109">Développez les dossiers **s0:getXhtmlResponse** et **getXhtmlResult**, puis faites glisser l'élément **MyRichTextElement** sur le formulaire. InfoPath reconnaîtra que **MyRichTextElement** est un élément XHTML et utilisera un contrôle de zone de texte enrichi pour la liaison à cet élément.</span><span class="sxs-lookup"><span data-stu-id="afb64-p109">Expand the **s0:getXhtmlResponse** and **getXhtmlResult** folders, and then drag the **MyRichTextElement** element onto the form. InfoPath will recognize that the **MyRichTextElement** element is an XHTML element and will use a rich text box control to bind to it.</span></span> 
    
15. <span data-ttu-id="afb64-148">Enregistrez ou publiez le formulaire.</span><span class="sxs-lookup"><span data-stu-id="afb64-148">Save or publish the form.</span></span>
    
<span data-ttu-id="afb64-p110">Pour tester le formulaire, ouvrez-le, insérez du contenu de type texte enrichi, par exemple des images, des tableaux et du texte mis en forme. Cliquez sur **Envoi** sur le ruban pour stocker ce contenu dans le fichier out.xml sur le serveur. Cliquez sur **Requête** sur l'onglet **Affichage**, puis cliquez sur le bouton **Exécuter la requête** dans le formulaire. Le contrôle **Zone de texte mis en forme** devrait afficher le contenu XHTML du fichier out.xml. Si le champ de texte enrichi contient plusieurs lignes, le service Web n'acceptera que la première ligne et ignorera le reste.</span><span class="sxs-lookup"><span data-stu-id="afb64-p110">To test the form, open the form, enter some rich text content such as pictures, tables, and formatted text. Click **Submit** on the ribbon to store the rich text content in the out.xml file on the server. Click **Query** on the **View** tab, and then click the **Run Query** button on the form. The **Rich Text Box** control should display the XHTML content from the out.xml file. If the rich text field contains multiple lines, the Web service will only accept the first line and ignore the rest.</span></span> 
  

