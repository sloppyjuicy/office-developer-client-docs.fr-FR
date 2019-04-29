---
title: Utilisation de MSXML et de System.Xml avec le modèle objet InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, using msxml5,MSXML5 [InfoPath 2007],MSXML5 script [InfoPath 2007],InfoPath 2007, using MSXML5
localization_priority: Normal
ms.assetid: f7a0cac5-26f9-49ed-b52c-0240ef0c9d38
description: Les projets de modèle de formulaire utilisant le modèle objet InfoPath 2003 utilisent en interne MSXML (Microsoft XML Core Services) pour travailler avec XML. Dans le code managé, il est souvent plus simple d'utiliser le support XML fourni par l'espace de noms System.Xml dans la bibliothèque de classes .NET Framework. MSXML et System.Xml ne peuvent pas échanger d'objets de façon native. Vous devez donc pour transférer des données XML entre InfoPath et un autre code managé convertir ces données XML. Vous pouvez échanger des données XML depuis les objets System.Xml avec du code de formulaire InfoPath à l'aide des techniques décrites dans cette rubrique.
ms.openlocfilehash: c56939a0cf03b5de6466de37013e154529afd1ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437398"
---
# <a name="working-with-msxml-and-systemxml-using-the-infopath-2003-object-model"></a><span data-ttu-id="44e24-107">Utilisation de MSXML et de System.Xml avec le modèle objet InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="44e24-107">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="44e24-p102">Les projets de modèle de formulaire utilisant le modèle objet InfoPath 2003 utilisent en interne MSXML (Microsoft XML Core Services) pour travailler avec XML. Dans le code managé, il est souvent plus simple d'utiliser le support XML fourni par l'espace de noms **System.Xml** dans la bibliothèque de classes .NET Framework. MSXML et **System.Xml** ne peuvent pas échanger d'objets de façon native. Vous devez donc pour transférer des données XML entre InfoPath et un autre code managé convertir ces données XML. Vous pouvez échanger des données XML depuis les objets **System.Xml** avec du code de formulaire InfoPath à l'aide des techniques décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="44e24-p102">Form template projects that work with the InfoPath 2003 object model use Microsoft XML Core Services (MSXML) internally to work with XML. In managed code, it is often easier to use the XML support provided by the **System.Xml** namespace in the .NET Framework class library. MSXML and **System.Xml** cannot exchange objects natively, so whenever you need to pass XML data between InfoPath and other managed code, XML data needs to be converted. You can exchange XML data from **System.Xml** objects with InfoPath form code by using the techniques in this topic.</span></span> 
  
<span data-ttu-id="44e24-112">Pour utiliser les membres de l'espace de noms **System.Xml** dans un projet de code managé qui utilise le modèle objet InfoPath 2003, vous devez ajouter une référence à **System.Xml** dans l'onglet **.NET** de la boîte de dialogue **Ajouter une référence** dans Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="44e24-112">To use members of the **System.Xml** namespace in a managed code project that uses the InfoPath 2003 object model, you must add a reference to **System.Xml** on the **.NET** tab of the **Add Reference** dialog box in Visual Studio 2012.</span></span> 
  
 <span data-ttu-id="44e24-113">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="44e24-113">**Notes**</span></span>
  
- <span data-ttu-id="44e24-114">Pour afficher des informations de référence sur MSXML, voir le MSXML SDK.</span><span class="sxs-lookup"><span data-stu-id="44e24-114">To view reference information about MSXML, see the MSXML SDK.</span></span>
    
- <span data-ttu-id="44e24-115">Les membres du modèle objet MSXML qui sont inclus par l'espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) ne peuvent pas être affectés à des délégués dans le code de formulaire des modèles de formulaires avec code managé.</span><span class="sxs-lookup"><span data-stu-id="44e24-115">Members of the MSXML object model that are wrapped by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace cannot be assigned to delegates in the form code of managed-code form templates.</span></span> 
    
- <span data-ttu-id="44e24-p103">Si vous mettez à jour le code de votre modèle de formulaire pour utiliser le modèle objet fourni par les membres de l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , **System.Xml** est utilisé en mode natif. Toutefois, dans ce cas, vous devez convertir manuellement l'ensemble de votre code pour pouvoir utiliser le nouveau modèle objet. Pour convertir votre modèle de formulaire afin d'utiliser le nouveau modèle d'objet, dans la catégorie **Programmation** de la boîte de dialogue **Options de formulaire**, cliquez sur **Mettre à niveau le modèle objet**.</span><span class="sxs-lookup"><span data-stu-id="44e24-p103">If you update the code of your form template to use the object model provided by members of the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace, **System.Xml** is used natively. However, when doing so, you must manually convert all of your code to use the new object model. To convert your form template to use the new object model, in the **Programming** category of the **Form Options** dialog box, click **Upgrade OM**.</span></span>
    
## <a name="loading-an-entire-xml-document-object-model-dom-from-systemxml"></a><span data-ttu-id="44e24-119">Chargement de l'intégralité du modèle objet de document XML (DOM) depuis System.Xml</span><span class="sxs-lookup"><span data-stu-id="44e24-119">Loading an Entire XML Document Object Model (DOM) from System.Xml</span></span>

<span data-ttu-id="44e24-120">L'exemple de code qui suit illustre comment charger l'intégralité d'un DOM XML depuis **System.Xml** à l'aide de la méthode InfoPath [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) et des membres de MSXML (Microsoft XML Core Services) incorporés dans l'espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) .</span><span class="sxs-lookup"><span data-stu-id="44e24-120">The following code sample demonstrates how to load an entire XML DOM from **System.Xml** code using the InfoPath [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) method and the members of Microsoft XML Core Services that are wrapped by members of the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
<span data-ttu-id="44e24-p104">Les exemples suivants requièrent une directive **using** ou **Imports** pour **System.Xml** dans la section des déclarations du module de code du formulaire. En outre, étant donné que la méthode **Load** de la classe **XmlDocument** requiert **System.Security.Permissions.FileIOPermission**, vous devez configurer le niveau de sécurité du modèle de formulaire sur **Autorisation totale** au moyen de la catégorie **Sécurité et approbation** de la boîte de dialogue **Options de formulaire**.</span><span class="sxs-lookup"><span data-stu-id="44e24-p104">The following examples require a **using** or **Imports** directive for **System.Xml** in the declarations section of the form code module. Additionally, because the **Load** method of the **XmlDocument** class requires **System.Security.Permissions.FileIOPermission**, you must configure the security level of the form template as **Full Trust** using the **Security and Trust** category of the **Form Options** dialog box.</span></span> 
  
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

## <a name="loading-a-single-node-from-systemxml"></a><span data-ttu-id="44e24-123">Chargement d'un seul nœud depuis System.Xml</span><span class="sxs-lookup"><span data-stu-id="44e24-123">Loading a Single Node from System.Xml</span></span>

<span data-ttu-id="44e24-p105">L'exemple de code qui suit présente une fonction qui démontre comment cloner un seul nœud depuis **System.Xml**. **XmlElement** à l'aide de la méthode MSXML incorporée **createNode**.</span><span class="sxs-lookup"><span data-stu-id="44e24-p105">The following code sample shows a function that demonstrates how to clone a single node from a **System.Xml**. **XmlElement** using the wrapped MSXML **createNode** method.</span></span> 
  
<span data-ttu-id="44e24-126">Les exemples suivants requièrent une directive **using** ou **Imports** pour **System.Xml** dans la section des déclarations du module de code du formulaire.</span><span class="sxs-lookup"><span data-stu-id="44e24-126">The following examples require a **using** or **Imports** directive for **System.Xml** in the declarations section of the form code module.</span></span> 
  
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


