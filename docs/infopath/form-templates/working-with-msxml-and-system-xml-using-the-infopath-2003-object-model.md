---
title: Utilisation de MSXML et de System.Xml avec le modèle objet InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, using msxml5,MSXML5 [InfoPath 2007],MSXML5 script [InfoPath 2007],InfoPath 2007, using MSXML5
ms.localizationpriority: medium
ms.assetid: f7a0cac5-26f9-49ed-b52c-0240ef0c9d38
description: Les projets de modèle de formulaire utilisant le modèle objet InfoPath 2003 utilisent en interne MSXML (Microsoft XML Core Services) pour travailler avec XML. Dans le code managé, il est souvent plus simple d'utiliser le support XML fourni par l'espace de noms System.Xml dans la bibliothèque de classes .NET Framework. MSXML et System.Xml ne peuvent pas échanger d'objets de façon native. Vous devez donc pour transférer des données XML entre InfoPath et un autre code managé convertir ces données XML. Vous pouvez échanger des données XML depuis les objets System.Xml avec du code de formulaire InfoPath à l'aide des techniques décrites dans cette rubrique.
ms.openlocfilehash: 7fa559974a542aeb3472f6ef51ac6869a94cf6d4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588370"
---
# <a name="working-with-msxml-and-systemxml-using-the-infopath-2003-object-model"></a>Utilisation de MSXML et de System.Xml avec le modèle objet InfoPath 2003

Les projets de modèle de formulaire utilisant le modèle objet InfoPath 2003 utilisent en interne MSXML (Microsoft XML Core Services) pour travailler avec XML. Dans le code managé, il est souvent plus simple d'utiliser le support XML fourni par l'espace de noms **System.Xml** dans la bibliothèque de classes .NET Framework. MSXML et **System.Xml** ne peuvent pas échanger d'objets de façon native. Vous devez donc pour transférer des données XML entre InfoPath et un autre code managé convertir ces données XML. Vous pouvez échanger des données XML depuis les objets **System.Xml** avec du code de formulaire InfoPath à l'aide des techniques décrites dans cette rubrique. 
  
Pour utiliser les membres de l'espace de noms **System.Xml** dans un projet de code managé qui utilise le modèle objet InfoPath 2003, vous devez ajouter une référence à **System.Xml** dans l'onglet **.NET** de la boîte de dialogue **Ajouter une référence** dans Visual Studio 2012. 
  
 **Remarques**
  
- Pour afficher des informations de référence sur MSXML, voir le MSXML SDK.
    
- Les membres du modèle objet MSXML qui sont inclus par l'espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) ne peuvent pas être affectés à des délégués dans le code de formulaire des modèles de formulaires avec code managé. 
    
- Si vous mettez à jour le code de votre modèle de formulaire pour utiliser le modèle objet fourni par les membres de l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , **System.Xml** est utilisé en mode natif. Toutefois, dans ce cas, vous devez convertir manuellement l'ensemble de votre code pour pouvoir utiliser le nouveau modèle objet. Pour convertir votre modèle de formulaire afin d'utiliser le nouveau modèle d'objet, dans la catégorie **Programmation** de la boîte de dialogue **Options de formulaire**, cliquez sur **Mettre à niveau le modèle objet**.
    
## <a name="loading-an-entire-xml-document-object-model-dom-from-systemxml"></a>Chargement de l'intégralité du modèle objet de document XML (DOM) depuis System.Xml

L'exemple de code qui suit illustre comment charger l'intégralité d'un DOM XML depuis **System.Xml** à l'aide de la méthode InfoPath [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) et des membres de MSXML (Microsoft XML Core Services) incorporés dans l'espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
  
Les exemples suivants requièrent une directive **using** ou **Imports** pour **System.Xml** dans la section des déclarations du module de code du formulaire. En outre, étant donné que la méthode **Load** de la classe **XmlDocument** requiert **System.Security.Permissions.FileIOPermission**, vous devez configurer le niveau de sécurité du modèle de formulaire sur **Autorisation totale** au moyen de la catégorie **Sécurité et approbation** de la boîte de dialogue **Options de formulaire**. 
  
```cs
// Create a System.Xml XmlDocument and load an XML file.
XmlDocument doc = new XmlDocument();
doc.Load("c:\\temp\\MyFile.xml");
// Create an MSXML DOM object.
IXMLDOMDocument newDoc = thisXDocument.CreateDOM();
// Load the DOM with the XML from the System.XML object.
newDoc.loadXML(doc.DocumentElement.OuterXml);
```

```vb
' Create a System.Xml XmlDocument and load an XML file.
Dim doc As XmlDocument = New XmlDocument()
doc.Load("c:\temp\MyFile.xml");
' Create an MSXML DOM object.
Dim newDoc As IXMLDOMDocument = thisXDocument.CreateDOM()
' Load the DOM with the XML from the System.XML object.
newDoc.loadXML(doc.DocumentElement.OuterXml)
```

## <a name="loading-a-single-node-from-systemxml"></a>Chargement d'un seul nœud depuis System.Xml

L'exemple de code qui suit présente une fonction qui démontre comment cloner un seul nœud depuis **System.Xml**. **XmlElement** à l'aide de la méthode MSXML incorporée **createNode**. 
  
Les exemples suivants requièrent une directive **using** ou **Imports** pour **System.Xml** dans la section des déclarations du module de code du formulaire. 
  
```cs
// This function takes a System.Xml XmlElement object and 
// an MSXML IXMLDOMDocument object, and returns an MSXML 
// IXMLDOMNode object that is a copy of the XmlElement object.
public IXMLDOMNode CloneSystemXmlElementToMsxml(
   XmlElement systemXmlElement, IXMLDOMDocument msxmlDocument)
{
   IXMLDOMNode msxmlResultNode;
   // Create a new element from the MSXML DOM using the same 
   // namespace as the XmlElement.
   msxmlResultNode = msxmlDocument.createNode(
      DOMNodeType.NODE_ELEMENT, 
      systemXmlElement.Name, 
      systemXmlElement.NamespaceURI);
   // Set the element's value.
   msxmlResultNode.text = systemXmlElement.Value.ToString();
   return msxmlResultNode;
}
```

```vb
' This function takes a System.Xml XmlElement object and 
' an MSXML IXMLDOMDocument object, and returns an MSXML 
' IXMLDOMNode object that is a copy of the XmlElement object.
Public Function CloneSystemXmlElementToMsxml(_
   XmlElement systemXmlElement, _
   IXMLDOMDocument msxmlDocument) As IXMLDOMNode
   Dim msxmlResultNode As IXMLDOMNode
   ' Create a new element from the MSXML DOM using the same 
   ' namespace as the XmlElement.
   msxmlResultNode = msxmlDocument.createNode(_
      DOMNodeType.NODE_ELEMENT, _
      systemXmlElement.Name, _
      systemXmlElement.NamespaceURI)
   ' Set the element's value.
   msxmlResultNode.text = systemXmlElement.Value.ToString()
   Return msxmlResultNode
End Function
```


