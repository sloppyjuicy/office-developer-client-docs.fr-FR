---
title: Section de schéma (référence de base de données du bureau Access)
TOCTitle: Schema Section
ms:assetid: 59b42ffb-0524-adc3-8bcd-6e4cd2c505ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249304(v=office.15)
ms:contentKeyID: 48545023
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 00a5c08784d1a57e148acbaa6f1621102d6b6712
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947755"
---
# <a name="schema-section"></a>Section de schéma

**S’applique à**: Access 2013, Office 2013

## <a name="schema-section"></a>Section Schema

La section Schema est obligatoire. Comme illustré dans l'exemple précédent,  ADO écrit des métadonnées détaillées concernant chaque colonne pour préserver au mieux la sémantique des valeurs en vue de leur mise à jour. Cependant, pour les charger dans le fichier XML, ADO a uniquement besoin des noms des colonnes et du jeu de lignes auquel elles appartiennent. Voici un exemple de schéma minimal :

```xml 
 
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882" 
    xmlns:rs="urn:schemas-microsoft-com:rowset" 
    xmlns:z="#RowsetSchema"> 
  <s:Schema id="RowsetSchema"> 
    <s:ElementType name="row" content="eltOnly"> 
      <s:AttributeType name="ShipperID"/> 
      <s:AttributeType name="CompanyName"/> 
      <s:AttributeType name="Phone"/> 
      <s:Extends type="rs:rowbase"/> 
    </s:ElementType> 
  </s:Schema> 
  <rs:data> 
... 
  </rs:data> 
</xml> 
```

Dans l'exemple précédent, ADO traite les données comme des chaînes de longueur variable parce qu'aucune information de type n'est incluse dans le schéma.

## <a name="creating-aliases-for-column-names"></a>Création d'alias pour les noms de colonnes

L'attribut **rs:name** vous permet de créer un alias d'un nom de colonne pour qu'un nom convivial puisse apparaître dans les informations de colonne exposées par le jeu de lignes et qu'un nom plus court puisse être utilisé dans la section de données. Le schéma ci-dessus peut, par exemple, être modifié pour mapper ShipperID et s1, CompanyName et s2, Phone et s3, comme suit :

```xml 
 
<s:Schema id="RowsetSchema">  
<s:ElementType name="row" content="eltOnly" rs:updatable="true">  
<s:AttributeType name="s1" rs:name="ShipperID" rs:number="1" ...>  
... 
</s:AttributeType>  
<s:AttributeType name="s2" rs:name="CompanyName" rs:number="2" ...>  
... 
</s:AttributeType>  
<s:AttributeType name="s3" rs:name="Phone" rs:number="3" ...>  
... 
</s:AttributeType>  
... 
</s:ElementType>  
</s:Schema>  
```

Ensuite, dans la section de données, la ligne utilise l'attribut **name** (et non **rs:name**) pour faire référence à cette colonne :

```xml 
 
"<row s1="1" s2="Speedy Express" s3="(503) 555-9831"/> 
```

La création d'alias pour les noms de colonnes est requise lorsqu'un nom de colonne n'est pas un attribut ou un nom de balise conforme dans XML. Par exemple, « Last Name » doit avoir un alias car les noms contenant des espaces incorporés ne sont pas des attributs conformes. Étant donné que la ligne suivante ne sera pas traitée correctement par l'analyseur XML, vous devez créer un alias d'un autre nom, sans espace incorporé :

```xml 
 
<row last name="Jones"/> 
```

La valeur utilisée pour l'attribut **name**, quelle qu'elle soit, doit être utilisée de façon systématique chaque fois que la colonne est référencée dans les sections relatives au schéma et aux données du document XML. L'exemple suivant illustre une utilisation cohérente de s1 :

```xml 
 
<s:Schema id="RowsetSchema"> 
  <s:ElementType name="row" content="eltOnly"> 
    <s:attribute type="s1"/> 
    <s:attribute type="CompanyName"/> 
    <s:attribute type="s3"/> 
    <s:extends type="rs:rowbase"/> 
  </s:ElementType> 
  <s:AttributeType name="s1" rs:name="ShipperID" rs:number="1"  
    rs:maydefer="true" rs:writeunknown="true"> 
    <s:datatype dt:type="i4" dt:maxLength="4" rs:precision="10"  
      rs:fixedlength="true" rs:maybenull="true"/> 
  </s:AttributeType> 
</s:Schema> 
<rs:data> 
  <z:row s1="1" CompanyName="Speedy Express" s3="(503) 555-9831"/> 
</rs:data> 
```

De la même façon, aucun alias n'étant défini pour CompanyName, CompanyName doit être utilisé de façon cohérente dans l'ensemble du document.

## <a name="data-types"></a>Types de données

Vous pouvez appliquer un type de données à une colonne avec l'attribut **dt:type**. Un type de données peut être défini de deux manières : soit en spécifiant directement l'attribut **dt:type** dans la définition de colonne proprement dite, soit en utilisant la construction **s:datatype** comme élément imbriqué de la définition de colonne. Par exemple,

```xml 
 
<s:AttributeType name="Phone" > 
  <s:datatype dt:type="string"/> 
</s:AttributeType> 
```

équivaut à

```xml 
 
<s:AttributeType name="Phone" dt:type="string"/> 
```

Si vous omettez complètement l'attribut **dt:type** dans la définition de ligne, le type de colonne sera, par défaut, une chaîne de longueur variable.

Si vous disposez d'informations sur le type autres que son nom (par exemple, **dt:maxLength**), l'utilisation de l'élément enfant **s:datatype** permettra d'améliorer la lisibilité. Notez qu'il s'agit là d'une convention, non d'une obligation.

Les exemples suivants illustrent l'insertion d'informations de type dans un schéma :

```xml 
 
<!-- 1. String with no max length --> 
<s:AttributeType name="title_id"/> 
<! — or --> 
<s:AttributeType name="title_id" dt:type="string"/> 
 
<! — 2. Fixed length string with max length of 6 --> 
<s:AttributeType name="title_id"> 
    <s:datatype dt:type="string" dt:maxLength="6" rs:fixedlength="true" /> 
</s:AttributeType> 
 
<! — 3. Variable length string with max length of 6 --> 
<s:AttributeType name="title_id"> 
    <s:datatype dt:type="string" dt:maxLength="6" /> 
</s:AttributeType> 
 
<! — 4. Integer --> 
<s:AttributeType name="title_id" dt:type="int"/> 
```

Le deuxième exemple présente une utilisation subtile de l'attribut **rs:fixedlength**. Une colonne dont l'attribut **rs:fixedlength** a la valeur True signifie que les données doivent avoir la longueur définie dans le schéma. Dans ce cas, la valeur pour le titre légalement\_id est « 123456 », comme c’est « 123 ». Toutefois, « 123 » ne sera pas une valeur conforme car sa longueur est de trois caractères et non six. Pour plus d'informations sur la propriété **fixedlength**, consultez le manuel OLE DB Programmer's Guide (en anglais).

## <a name="handling-nulls"></a>Gestion des valeurs Null

Les valeurs NULL sont gérées par l'attribut **rs:maybenull**. Si cet attribut a la valeur True, le contenu de la colonne peut contenir une valeur Null. En outre, si la colonne est introuvable dans une ligne de données et que l'utilisateur lit les données dans le jeu de lignes, **IRowset::GetData()** retourne un état Null. Observez les définitions de colonnes de la table Shippers suivantes :

```xml 
 
<s:AttributeType name="ShipperID"> 
  <s:datatype dt:type="int" dt:maxLength="4"/> 
</s:AttributeType> 
<s:AttributeType name="CompanyName"> 
  <s:datatype dt:type="string" dt:maxLength="40" rs:maybenull="true"/> 
</s:AttributeType> 
```

D'après la définition, la valeur CompanyName peut être Null, mais le champ ShipperID ne peut contenir de valeur Null. Si la section données contenue la ligne suivante, le fournisseur de persistance doit définir l’état des données pour la colonne CompanyName à la constante d’état OLE DB DBSTATUS\_S\_ISNULL :

```xml 
 
<z:row ShipperID="1"/> 
```

Si la ligne était complètement vide, comme suit, le fournisseur de persistance retourne l’état OLE DB DBSTATUS\_E\_non disponible pour ShipperID et DBSTATUS\_S\_ISNULL pour CompanyName.

```xml 
 
<z:row/>  
```

Notez qu'une chaîne vide (de longueur nulle) n'équivaut pas à une chaîne de valeur Null.

```xml 
 
<z:row ShipperID="1" CompanyName=""/> 
```

Pour la ligne précédente, le fournisseur de persistance retourne l’état OLE DB DBSTATUS\_S\_OK pour les deux colonnes. Dans ce cas, la valeur de la colonne CompanyName est simplement "" (une chaîne vide).

Pour plus d'informations sur les constructions OLE DB utilisables dans le schéma d'un document XML pour OLE DB, reportez-vous à la définition de « "urn:schemas-microsoft-com:rowset » et au manuel OLE DB Programmer's Guide (en anglais).

