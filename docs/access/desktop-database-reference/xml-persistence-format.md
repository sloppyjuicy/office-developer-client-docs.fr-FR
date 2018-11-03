---
title: Format de persistance XML
TOCTitle: XML Persistence Format
ms:assetid: 499f335c-ee1f-c803-e3a8-034b8decf1ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249226(v=office.15)
ms:contentKeyID: 48544643
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 291a75fb88690a5674d872f2adb01b683f5e99bd
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946712"
---
# <a name="xml-persistence-format"></a><span data-ttu-id="54e30-102">Format de persistance XML</span><span class="sxs-lookup"><span data-stu-id="54e30-102">XML persistence format</span></span>

<span data-ttu-id="54e30-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="54e30-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="xml-persistence-format"></a><span data-ttu-id="54e30-104">Format de persistance XML</span><span class="sxs-lookup"><span data-stu-id="54e30-104">XML Persistence Format</span></span>

<span data-ttu-id="54e30-105">ADO utilise le codage UTF-8 pour le flux de données XML.</span><span class="sxs-lookup"><span data-stu-id="54e30-105">ADO uses UTF-8 encoding for the XML stream it persists.</span></span>

<span data-ttu-id="54e30-p101">Le format XML ADO se compose de deux sections, une section de schéma suivie d'une section de données. Vous trouverez ci-après un exemple de fichier XML pour la table Messagers de la base de données Les comptoirs. Certains éléments du fichier XML sont expliqués à la suite de l'exemple.</span><span class="sxs-lookup"><span data-stu-id="54e30-p101">The ADO XML format is broken into two sections, a schema section followed by the data section. The following is an example XML file for the Shippers table from the Northwind database. Various parts of the XML are discussed following the example.</span></span>

```xml
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"  
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"  
xmlns:rs="urn:schemas-microsoft-com:rowset"  
xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="ShipperID" rs:number="1"  
        rs:basetable="shippers" rs:basecolumn="ShipperID" 
        rs:keycolumn="true">  
        <s:datatype dt:type="int" dt:maxLength="4" rs:precision="10"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="CompanyName" rs:number="2"  
        rs:nullable="true" rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="CompanyName">  
        <s:datatype dt:type="string" dt:maxLength="40" />  
      </s:AttributeType>  
      <s:AttributeType name="Phone" rs:number="3" rs:nullable="true"  
        rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="Phone">  
        <s:datatype dt:type="string" dt:maxLength="24"/>  
      </s:AttributeType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
 
  <rs:data>  
    <z:row ShipperID="1" CompanyName="Speedy Express"  
      Phone="(503) 555-9831"/>  
    <z:row ShipperID="2" CompanyName="United Package"  
      Phone="(503) 555-3199"/>  
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/>  
  </rs:data>  
</xml> 
```

<span data-ttu-id="54e30-p102">Le schéma montre les déclarations des espaces de noms, la section des schémas et la section des données. La section des schémas contient la définition de ligne, de ShipperID, de CompanyName et de Phone.</span><span class="sxs-lookup"><span data-stu-id="54e30-p102">The schema shows the declarations of namespaces, the schema section, and the data section. The schema section contains definitions for row, ShipperID, CompanyName, and Phone.</span></span>

<span data-ttu-id="54e30-p103">Les définitions des schémas sont conformes à la spécification XML-Data et peuvent être entièrement validées (cette validation ne peut se faire avec Internet Explorer 5). Pour prendre connaissance de cette spécification, allez sur [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-Data est le seul format de schéma existant actuellement pour la persistance **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="54e30-p103">Schema definitions conform to the XML-Data specification and are able to be fully validated (though validation will not occur in Internet Explorer 5). You can view this specification at [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-Data is the only supported schema format for **Recordset** persistence currently.</span></span>

<span data-ttu-id="54e30-114">La section des données possède trois lignes contenant des informations sur les messagers.</span><span class="sxs-lookup"><span data-stu-id="54e30-114">The data section has three rows containing information about shippers.</span></span> <span data-ttu-id="54e30-115">Pour un ensemble de lignes vide, la section de données peut être vide, mais le `<rs:data>` balises doivent être présents.</span><span class="sxs-lookup"><span data-stu-id="54e30-115">For an empty rowset, the data section may be empty, but the `<rs:data>` tags must be present.</span></span> <span data-ttu-id="54e30-116">Sans données, vous pouvez écrire la balise comme simplement `<rs:data>`.</span><span class="sxs-lookup"><span data-stu-id="54e30-116">With no data, you could write the tag shorthand as simply `<rs:data>`.</span></span> <span data-ttu-id="54e30-117">Les balises précédées du préfixe "rs" sont placées dans l'espace de nom défini par urn:schemas-microsoft-com:rowset.</span><span class="sxs-lookup"><span data-stu-id="54e30-117">Any tag prefixed with "rs" indicates that it is in the namespace defined by urn:schemas-microsoft-com:rowset.</span></span> <span data-ttu-id="54e30-118">La définition complète de ce schéma est définie en annexe de ce document.</span><span class="sxs-lookup"><span data-stu-id="54e30-118">The full definition of this schema is defined in the appendix to this document.</span></span>

## <a name="xml-persistence-format"></a><span data-ttu-id="54e30-119">Format de persistance XML</span><span class="sxs-lookup"><span data-stu-id="54e30-119">XML Persistence Format</span></span>

<span data-ttu-id="54e30-120">ADO utilise le codage UTF-8 pour le flux de données XML.</span><span class="sxs-lookup"><span data-stu-id="54e30-120">ADO uses UTF-8 encoding for the XML stream it persists.</span></span>

<span data-ttu-id="54e30-p105">Le format XML ADO se compose de deux sections, une section de schéma suivie d'une section de données. Vous trouverez ci-après un exemple de fichier XML pour la table Messagers de la base de données Les comptoirs. Certains éléments du fichier XML sont expliqués à la suite de l'exemple.</span><span class="sxs-lookup"><span data-stu-id="54e30-p105">The ADO XML format is broken into two sections, a schema section followed by the data section. The following is an example XML file for the Shippers table from the Northwind database. Various parts of the XML are discussed following the example.</span></span>

```xml
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"  
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"  
xmlns:rs="urn:schemas-microsoft-com:rowset"  
xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="ShipperID" rs:number="1"  
        rs:basetable="shippers" rs:basecolumn="ShipperID" 
        rs:keycolumn="true">  
        <s:datatype dt:type="int" dt:maxLength="4" rs:precision="10"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="CompanyName" rs:number="2"  
        rs:nullable="true" rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="CompanyName">  
        <s:datatype dt:type="string" dt:maxLength="40" />  
      </s:AttributeType>  
      <s:AttributeType name="Phone" rs:number="3" rs:nullable="true"  
        rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="Phone">  
        <s:datatype dt:type="string" dt:maxLength="24"/>  
      </s:AttributeType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
 
  <rs:data>  
    <z:row ShipperID="1" CompanyName="Speedy Express"  
      Phone="(503) 555-9831"/>  
    <z:row ShipperID="2" CompanyName="United Package"  
      Phone="(503) 555-3199"/>  
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/>  
  </rs:data>  
</xml> 
```

<span data-ttu-id="54e30-p106">Le schéma montre les déclarations des espaces de noms, la section des schémas et la section des données. La section des schémas contient la définition de ligne, de ShipperID, de CompanyName et de Phone.</span><span class="sxs-lookup"><span data-stu-id="54e30-p106">The schema shows the declarations of namespaces, the schema section, and the data section. The schema section contains definitions for row, ShipperID, CompanyName, and Phone.</span></span>

<span data-ttu-id="54e30-p107">Les définitions des schémas sont conformes à la spécification XML-Data et peuvent être entièrement validées (cette validation ne peut se faire avec Internet Explorer 5). Pour prendre connaissance de cette spécification, allez sur [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-Data est le seul format de schéma existant actuellement pour la persistance **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="54e30-p107">Schema definitions conform to the XML-Data specification and are able to be fully validated (though validation will not occur in Internet Explorer 5). You can view this specification at [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-Data is the only supported schema format for **Recordset** persistence currently.</span></span>

<span data-ttu-id="54e30-129">La section des données possède trois lignes contenant des informations sur les messagers.</span><span class="sxs-lookup"><span data-stu-id="54e30-129">The data section has three rows containing information about shippers.</span></span> <span data-ttu-id="54e30-130">Pour un ensemble de lignes vide, la section de données peut être vide, mais le `<rs:data>` balises doivent être présents.</span><span class="sxs-lookup"><span data-stu-id="54e30-130">For an empty rowset, the data section may be empty, but the `<rs:data>` tags must be present.</span></span> <span data-ttu-id="54e30-131">Sans données, vous pouvez écrire la balise comme simplement `<rs:data>`.</span><span class="sxs-lookup"><span data-stu-id="54e30-131">With no data, you could write the tag shorthand as simply `<rs:data>`.</span></span> <span data-ttu-id="54e30-132">Les balises précédées du préfixe "rs" sont placées dans l'espace de nom défini par urn:schemas-microsoft-com:rowset.</span><span class="sxs-lookup"><span data-stu-id="54e30-132">Any tag prefixed with "rs" indicates that it is in the namespace defined by urn:schemas-microsoft-com:rowset.</span></span> <span data-ttu-id="54e30-133">La définition complète de ce schéma est définie en annexe de ce document.</span><span class="sxs-lookup"><span data-stu-id="54e30-133">The full definition of this schema is defined in the appendix to this document.</span></span>

