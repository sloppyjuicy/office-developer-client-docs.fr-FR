---
title: Texte enrichi et services Web
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 53fddc3f-e9d9-db76-6b84-11befdb23fb0
description: "Microsoft InfoPath prend en charge la liaison d'un contrôle Zone de texte mis en forme dans un formulaire à un élément XML reçu à partir d'un service Web, ainsi que l'envoi de données à partir d'un tel contrôle vers un élément XML via un service Web. L'élément doit respecter le format XHTML (Extensible HyperText Markup Language). Par exemple, le schéma d'un élément nommé MyRichTextElement qui contient du texte enrichi aurait la définition de schéma XML suivante :"
ms.openlocfilehash: d10f4a8cedcff43d1c351068859aee0edf607c81
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391814"
---
# <a name="rich-text-and-web-services"></a>Texte enrichi et services Web

Microsoft InfoPath prend en charge la liaison d'un contrôle **Zone de texte mis en forme** dans un formulaire à un élément XML reçu à partir d'un service Web, ainsi que l'envoi de données à partir d'un tel contrôle vers un élément XML via un service Web. L'élément doit respecter le format XHTML (Extensible HyperText Markup Language). Par exemple, le schéma d'un élément nommé  `MyRichTextElement` qui contient du texte enrichi aurait la définition de schéma XML suivante : 
  
```XML
<xsd:element name="MyRichTextElement"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="https://www.w3.org/1999/xhtml" processContents="lax" 
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element>
```

Pour pouvoir lier un contrôle **Zone de texte mis en forme** à l'élément XHTML, cet élément doit être incorporé dans un nœud wrapper ; ce nœud peut appartenir à un espace de noms arbitraire et ressembler à ce qui suit : 
  
```xml
<xhtmlNode xmlns="https:// someNamespace"> 
    <div xmlns="https://www.w3.org/1999/xhtml">Your rich text here</div> 
</xhtmlNode>
```

Cette rubrique donne une vue d'ensemble du processus de création d'un service Web qui peut envoyer et recevoir du code XHTML. Elle présente également comment utiliser InfoPath pour effectuer la liaison aux paramètres du service Web. Mais, elle ne donne pas la procédure détaillée pour créer un tel service Web. Il est supposé que vous avez des connaissances sur l'utilisation des services Web.
  
## <a name="how-to-design-a-web-service-to-receive-and-send-xhtml"></a>Comment concevoir un service Web pour recevoir et envoyer du code XHTML

Le service Web en exemple stocke les données XHTML qu'il envoie et reçoit dans un fichier XML sur le serveur. Ce fichier, nommé out.xml, agit comme une source de données qui stocke les données XHTML. Deux méthodes Web qui seront présentées permettent d'interfacer une application cliente avec la source de données XHTML :  `getXhtml` et  `setXhtml`. La méthode  `getXhtml` de service Web retourne un **XmlNode** qui contient le code XHTML qui peut être lié à un contrôle de zone de texte enrichi InfoPath. La méthode  `setXhtml` de service Web accepte un **XmlNode** en tant que données à stocker dans le fichier out.xml. 
  
> [!NOTE]
> [!REMARQUE] Ces méthodes Web requièrent des déclarations **using** pour faire référence aux espaces de noms **System.IO** et **System.Xml**. 
  
La méthode  `getXhtml` de service Web essaie de charger les données XML à renvoyer à partir du fichier out.xml situé dans le dossier Data sur le lecteur C. Si elle échoue, parce que le fichier est introuvable ou ne contient pas du code XML valide, elle retourne un élément HTML **DIV** vide qui fait référence à l'espace de noms XHTML. 
  
```cs
[WebMethod]
public XmlNode getXhtml()  
{  
            // This is the returned XmlDocument upon Query from InfoPath 
            XmlDocument document = new XmlDocument(); 
 
            // Create a wrapping node with the name of the rich text field. 
            // The "https://someNameSpace" can be any arbitrary namespace 
            XmlNode richNode = document.CreateNode 
                        (XmlNodeType.Element, "MyRichTextElement", "https://someNameSpace"); 
 
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
                tempDocument.LoadXml("<div xmlns=\"https://www.w3.org/1999/xhtml\"></div>"); 
            } 
 
            // Add the file content to the xml 
            richNode.AppendChild 
                        (document.ImportNode(tempDocument.DocumentElement, true)); 
 
            return richNode; 
}  

```

La méthode  `setXhtml` de service Web accepte le code XHTML d'un contrôle **Zone de texte mis en forme** sur un formulaire InfoPath. Comme les services Web ne prennent pas en charge de liste de nœuds, lorsqu'un champ de texte enrichi contenant plusieurs lignes est envoyé à un service Web, ce dernier n'accepte que la première ligne et ignore le reste. 
  
La méthode  `setXhtml` en exemple suppose qu'elle recevra un nœud XML de niveau supérieur, qui dans la plupart des cas sera incorporé dans un élément **DIV**. Si le code XML reçu ne contient pas d'élément englobant, par exemple lorsque le texte à l'intérieur du contrôle **Zone de texte mis en forme** n'est pas formaté, cette méthode le détectera en vérifiant si la propriété **NodeType** indique que le code XML transmis est un nœud de texte, auquel cas elle crée un élément **DIV** et copie le contenu du nœud de texte dans l'élément **DIV** afin que le **DIV**contienne un nœud de texte enfant avec le texte qui avait été envoyé au service Web. Le code XML reçu par cette méthode est écrit dans le fichier out.xml situé dans le dossier Data sur le lecteur C. 
  
> [!NOTE]
> [!REMARQUE] La méthode  `setXhtml` en exemple a été conçue pour accepter des données XHTML de toutes tailles. Dans la pratique, vérifiez systématiquement la quantité de données envoyées et fixez une limite supérieure pour celle-ci. 
  
```cs
[WebMethod]  
public void setXhtml(XmlNode xn)  
{  
            XmlDocument document = new XmlDocument(); 
 
            if (xn == null) 
            { 
                // If nothing was submitted or the rich text field is empty, 
                // create a DIV that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "https://www.w3.org/1999/xhtml"); 
                // Copy the node to our own XmlDocument 
                document.AppendChild(div); 
            } 
            if (xn.NodeType == XmlNodeType.Text) 
            { 
                // If plain text is passed in, wrap it in a DIV 
                // that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "https://www.w3.org/1999/xhtml"); 
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

## <a name="how-to-create-an-infopath-form-that-exchanges-data-with-the-sample-web-service"></a>Comment créer un formulaire InfoPath qui échange des données avec le service Web en exemple

Pour créer un formulaire afin de tester le service Web en exemple, procédez comme suit.
  
### <a name="to-create-a-form-that-connects-to-the-sample-web-service"></a>Pour créer un formulaire qui se connecte au service Web en exemple

1. Ouvrez le concepteur de formulaires InfoPath.
    
2. Sur l'onglet **Nouveau**, double-cliquez sur **Service Web** sous **Modèles de formulaires avancés**.
    
3. Dans la boîte de dialogue **Assistant Connexion de données**, cliquez sur **Réception des données**, puis sur **Suivant**.
    
4. Tapez l'adresse du service Web qui contient les méthodes du service Web en exemple, puis cliquez sur **Suivant**. 
    
5. Pour la méthode de réception, sélectionnez **getXhtml** comme opération, puis cliquez sur **Suivant**.
    
6. La méthode de service Web **getXHTML** ne prenant aucun paramètre en charge, cliquez sur **Suivant**.
    
7. Cliquez sur **Terminer**.
    
8. Sur l'onglet **Données**, dans le groupe **Actions d'envoi**, cliquez sur **À d'autres emplacements**, puis sur **Service Web** afin d'utiliser le même service Web pour l'envoi des données. 
    
9. Tapez l'adresse du service Web qui contient les méthodes du service Web en exemple, puis cliquez sur **Suivant**.
    
10. Pour la méthode d'envoi, sélectionnez **setXhtml** comme opération, puis cliquez sur **Suivant**.
    
11. Cliquez sur **Modifier**, développez le dossier **dataFields**, puis le dossier **s0:getXhtmlResponse**, puis le dossier **getXhtmlResult**, sélectionnez l'élément **MyRichTextElement**, puis cliquez sur **Suivant**.
    
12. Cliquez sur **Terminer**.
    
13. Dans le volet Office **Champs**, développez le dossier **dataFields**. 
    
14. Développez les dossiers **s0:getXhtmlResponse** et **getXhtmlResult**, puis faites glisser l'élément **MyRichTextElement** sur le formulaire. InfoPath reconnaîtra que **MyRichTextElement** est un élément XHTML et utilisera un contrôle de zone de texte enrichi pour la liaison à cet élément. 
    
15. Enregistrez ou publiez le formulaire.
    
Pour tester le formulaire, ouvrez-le, insérez du contenu de type texte enrichi, par exemple des images, des tableaux et du texte mis en forme. Cliquez sur **Envoi** sur le ruban pour stocker ce contenu dans le fichier out.xml sur le serveur. Cliquez sur **Requête** sur l'onglet **Affichage**, puis cliquez sur le bouton **Exécuter la requête** dans le formulaire. Le contrôle **Zone de texte mis en forme** devrait afficher le contenu XHTML du fichier out.xml. Si le champ de texte enrichi contient plusieurs lignes, le service Web n'acceptera que la première ligne et ignorera le reste. 
  

