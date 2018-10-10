---
title: Format de persistance XML
TOCTitle: XML Persistence Format
ms:assetid: 499f335c-ee1f-c803-e3a8-034b8decf1ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249226(v=office.15)
ms:contentKeyID: 48544643
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9db8da66ab2c7bae1f28271ae37573f06ca222d7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470873"
---
# <a name="xml-persistence-format"></a>Format de persistance XML

**S’applique à**: Access 2013 | Office 2013

## <a name="xml-persistence-format"></a>Format de persistance XML

ADO utilise le codage UTF-8 pour le flux de données XML.

Le format XML ADO se compose de deux sections, une section de schéma suivie d'une section de données. Vous trouverez ci-après un exemple de fichier XML pour la table Messagers de la base de données Les comptoirs. Certains éléments du fichier XML sont expliqués à la suite de l'exemple.

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

Le schéma montre les déclarations des espaces de noms, la section des schémas et la section des données. La section des schémas contient la définition de ligne, de ShipperID, de CompanyName et de Phone.

Les définitions des schémas sont conformes à la spécification XML-Data et peuvent être entièrement validées (cette validation ne peut se faire avec Internet Explorer 5). Pour prendre connaissance de cette spécification, allez sur [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-Data est le seul format de schéma existant actuellement pour la persistance **Recordset**.

La section des données possède trois lignes contenant des informations sur les messagers. Pour un ensemble de lignes vide, la section de données peut être vide, mais le `<rs:data>` balises doivent être présents. Sans données, vous pouvez écrire la balise comme simplement `<rs:data>`. Les balises précédées du préfixe "rs" sont placées dans l'espace de nom défini par urn:schemas-microsoft-com:rowset. La définition complète de ce schéma est définie en annexe de ce document.

## <a name="xml-persistence-format"></a>Format de persistance XML

ADO utilise le codage UTF-8 pour le flux de données XML.

Le format XML ADO se compose de deux sections, une section de schéma suivie d'une section de données. Vous trouverez ci-après un exemple de fichier XML pour la table Messagers de la base de données Les comptoirs. Certains éléments du fichier XML sont expliqués à la suite de l'exemple.

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

Le schéma montre les déclarations des espaces de noms, la section des schémas et la section des données. La section des schémas contient la définition de ligne, de ShipperID, de CompanyName et de Phone.

Les définitions des schémas sont conformes à la spécification XML-Data et peuvent être entièrement validées (cette validation ne peut se faire avec Internet Explorer 5). Pour prendre connaissance de cette spécification, allez sur [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-Data est le seul format de schéma existant actuellement pour la persistance **Recordset**.

La section des données possède trois lignes contenant des informations sur les messagers. Pour un ensemble de lignes vide, la section de données peut être vide, mais le `<rs:data>` balises doivent être présents. Sans données, vous pouvez écrire la balise comme simplement `<rs:data>`. Les balises précédées du préfixe "rs" sont placées dans l'espace de nom défini par urn:schemas-microsoft-com:rowset. La définition complète de ce schéma est définie en annexe de ce document.

