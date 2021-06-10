---
title: Section Schéma (référence de base de données de bureau Access)
TOCTitle: Schema Section
ms:assetid: 59b42ffb-0524-adc3-8bcd-6e4cd2c505ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249304(v=office.15)
ms:contentKeyID: 48545023
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f8c479c430dd6d0ca742fefb4948544d31ba2e61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308938"
---
# <a name="schema-section"></a><span data-ttu-id="1b284-102">Section Schéma</span><span class="sxs-lookup"><span data-stu-id="1b284-102">Schema section</span></span>

<span data-ttu-id="1b284-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b284-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="schema-section"></a><span data-ttu-id="1b284-104">Section Schema</span><span class="sxs-lookup"><span data-stu-id="1b284-104">Schema Section</span></span>

<span data-ttu-id="1b284-p101">La section Schema est obligatoire. Comme illustré dans l'exemple précédent, ADO écrit des métadonnées détaillées concernant chaque colonne pour préserver au mieux la sémantique des valeurs en vue de leur mise à jour. Cependant, pour les charger dans le fichier XML, ADO a uniquement besoin des noms des colonnes et du jeu de lignes auquel elles appartiennent. Voici un exemple de schéma minimal :</span><span class="sxs-lookup"><span data-stu-id="1b284-p101">The schema section is required. As the previous example shows, ADO writes out detailed metadata about each column to preserve the semantics of the data values as much as possible for updating. However, to load in the XML, ADO only requires the names of the columns and the rowset to which they belong. Here is an example of a minimal schema:</span></span>

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

<span data-ttu-id="1b284-109">Dans l'exemple précédent, ADO traite les données comme des chaînes de longueur variable parce qu'aucune information de type n'est incluse dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="1b284-109">In the case above, ADO will treat the data as variable length strings because no type information is included in the schema.</span></span>

## <a name="creating-aliases-for-column-names"></a><span data-ttu-id="1b284-110">Création d'alias pour les noms de colonnes</span><span class="sxs-lookup"><span data-stu-id="1b284-110">Creating Aliases for Column Names</span></span>

<span data-ttu-id="1b284-p102">L'attribut **rs:name**  vous permet de créer un alias d'un nom de colonne pour qu'un nom convivial puisse apparaître dans les informations de colonne exposées par le jeu de lignes et qu'un nom plus court puisse être utilisé dans la section de données. Le schéma ci-dessus peut, par exemple, être modifié pour mapper ShipperID et s1, CompanyName et s2, Phone et s3, comme suit :</span><span class="sxs-lookup"><span data-stu-id="1b284-p102">The **rs:name** attribute allows you to create an alias for a column name so that a friendly name may appear in the column information exposed by the rowset and a shorter name may be used in the data section. For example, the schema above could be modified to map ShipperID to s1, CompanyName to s2, and Phone to s3 as follows:</span></span>

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

<span data-ttu-id="1b284-113">Ensuite, dans la section de données, la ligne utilise l'attribut **name** (et non **rs:name**) pour faire référence à cette colonne :</span><span class="sxs-lookup"><span data-stu-id="1b284-113">Then, in the data section, the row would use the **name** attribute (not **rs:name**) to refer to that column:</span></span>

```xml 
 
"<row s1="1" s2="Speedy Express" s3="(503) 555-9831"/> 
```

<span data-ttu-id="1b284-p103">La création d'alias pour les noms de colonnes est requise lorsqu'un nom de colonne n'est pas un attribut ou un nom de balise conforme dans XML. Par exemple, « Last Name » doit avoir un alias car les noms contenant des espaces incorporés ne sont pas des attributs conformes. Étant donné que la ligne suivante ne sera pas traitée correctement par l'analyseur XML, vous devez créer un alias d'un autre nom, sans espace incorporé :</span><span class="sxs-lookup"><span data-stu-id="1b284-p103">Creating aliases for column names is required whenever a column name is not a legal attribute or tag name in XML. For example, "Last Name" must have an alias because names with embedded spaces are illegal attributes. The following line won't be correctly handled by the XML parser, so you must create an alias to some other name that does not have an embedded space:</span></span>

```xml 
 
<row last name="Jones"/> 
```

<span data-ttu-id="1b284-p104">La valeur utilisée pour l'attribut **name**, quelle qu'elle soit, doit être utilisée de façon systématique chaque fois que la colonne est référencée dans les sections relatives au schéma et aux données du document XML. L'exemple suivant illustre une utilisation cohérente de s1 :</span><span class="sxs-lookup"><span data-stu-id="1b284-p104">Whatever value you use for the **name** attribute must be used consistently in each place that the column is referenced in both the schema and data sections of the XML document. The following example shows the consistent use of s1:</span></span>

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

<span data-ttu-id="1b284-119">De la même façon, aucun alias n'étant défini pour CompanyName, CompanyName doit être utilisé de façon cohérente dans l'ensemble du document.</span><span class="sxs-lookup"><span data-stu-id="1b284-119">Similarly, because there is no alias defined for CompanyName above, CompanyName must be used consistently throughout the document.</span></span>

## <a name="data-types"></a><span data-ttu-id="1b284-120">Types de données</span><span class="sxs-lookup"><span data-stu-id="1b284-120">Data Types</span></span>

<span data-ttu-id="1b284-p105">Vous pouvez appliquer un type de données à une colonne avec l'attribut **dt:type**. Un type de données peut être défini de deux manières : soit en spécifiant directement l'attribut **dt:type** dans la définition de colonne proprement dite, soit en utilisant la construction **s:datatype** comme élément imbriqué de la définition de colonne. Par exemple,</span><span class="sxs-lookup"><span data-stu-id="1b284-p105">You can apply a data type to a column with the **dt:type** attribute. You can specify a data type in two ways: either specify the **dt:type** attribute directly on the column definition itself or use the **s:datatype** construct as a nested element of the column definition. For example,</span></span>

```xml 
 
<s:AttributeType name="Phone" > 
  <s:datatype dt:type="string"/> 
</s:AttributeType> 
```

<span data-ttu-id="1b284-124">équivaut à</span><span class="sxs-lookup"><span data-stu-id="1b284-124">is equivalent to</span></span>

```xml 
 
<s:AttributeType name="Phone" dt:type="string"/> 
```

<span data-ttu-id="1b284-125">Si vous omettez complètement l'attribut **dt:type** dans la définition de ligne, le type de colonne sera, par défaut, une chaîne de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="1b284-125">If you omit the **dt:type** attribute entirely from the row definition, by default, the column's type will be a variable length string.</span></span>

<span data-ttu-id="1b284-p106">Si vous disposez d'informations sur le type autres que son nom (par exemple, **dt:maxLength**), l'utilisation de l'élément enfant **s:datatype** permettra d'améliorer la lisibilité. Notez qu'il s'agit là d'une convention, non d'une obligation.</span><span class="sxs-lookup"><span data-stu-id="1b284-p106">If you have more type information than simply the type name (for example, **dt:maxLength**), it makes it more readable to use the **s:datatype** child element. This is merely a convention, however, and not a requirement.</span></span>

<span data-ttu-id="1b284-128">Les exemples suivants illustrent l'insertion d'informations de type dans un schéma :</span><span class="sxs-lookup"><span data-stu-id="1b284-128">The following examples show further how to include type information in your schema:</span></span>

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

<span data-ttu-id="1b284-129">Le deuxième exemple présente une utilisation subtile de l'attribut **rs:fixedlength**.</span><span class="sxs-lookup"><span data-stu-id="1b284-129">There is a subtle use of the **rs:fixedlength** attribute in the second example.</span></span> <span data-ttu-id="1b284-130">Une colonne dont l'attribut **rs:fixedlength** a la valeur True signifie que les données doivent avoir la longueur définie dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="1b284-130">A column with the **rs:fixedlength** attribute set to true means that the data must have the length defined in the schema.</span></span> <span data-ttu-id="1b284-131">Dans ce cas, une valeur légale pour l’ID de titre est « \_ 123456 », tout comme « 123 ».</span><span class="sxs-lookup"><span data-stu-id="1b284-131">In this case, a legal value for title\_id is "123456," as is "123 ."</span></span> <span data-ttu-id="1b284-132">Toutefois, « 123 » ne sera pas une valeur conforme car sa longueur est de trois caractères et non six.</span><span class="sxs-lookup"><span data-stu-id="1b284-132">However, "123" would not be valid because its length is 3, not 6.</span></span> <span data-ttu-id="1b284-133">Pour plus d'informations sur la propriété **fixedlength**, consultez le manuel OLE DB Programmer's Guide (en anglais).</span><span class="sxs-lookup"><span data-stu-id="1b284-133">See the OLE DB Programmer's Guide for a more complete description of the **fixedlength** property.</span></span>

## <a name="handling-nulls"></a><span data-ttu-id="1b284-134">Gestion des valeurs Null</span><span class="sxs-lookup"><span data-stu-id="1b284-134">Handling Nulls</span></span>

<span data-ttu-id="1b284-p108">Les valeurs NULL sont gérées par l'attribut **rs:maybenull**. Si cet attribut a la valeur True, le contenu de la colonne peut contenir une valeur Null. En outre, si la colonne est introuvable dans une ligne de données et que l'utilisateur lit les données dans le jeu de lignes, **IRowset::GetData()** retourne un état Null. Observez les définitions de colonnes de la table Shippers suivantes :</span><span class="sxs-lookup"><span data-stu-id="1b284-p108">Null values are handled by the **rs:maybenull** attribute. If this attribute is set to true, the contents of the column may contain a null value. Furthermore, if the column is not found in a row of data, the user reading the data back from the rowset will get a null status from **IRowset::GetData()**. Consider the following column definitions from the Shippers table:</span></span>

```xml 
 
<s:AttributeType name="ShipperID"> 
  <s:datatype dt:type="int" dt:maxLength="4"/> 
</s:AttributeType> 
<s:AttributeType name="CompanyName"> 
  <s:datatype dt:type="string" dt:maxLength="40" rs:maybenull="true"/> 
</s:AttributeType> 
```

<span data-ttu-id="1b284-139">D'après la définition, la valeur CompanyName peut être Null, mais le champ ShipperID ne peut contenir de valeur Null.</span><span class="sxs-lookup"><span data-stu-id="1b284-139">The definition allows CompanyName to be null, but ShipperID cannot contain a null value.</span></span> <span data-ttu-id="1b284-140">Si la section de données contenait la ligne suivante, le fournisseur de persistance définirait l’état des données de la colonne CompanyName sur la constante d’état OLE DBSTATUS \_ S \_ ISNULL :</span><span class="sxs-lookup"><span data-stu-id="1b284-140">If the data section contained the following row, the Persistence Provider would set the status of the data for the CompanyName column to the OLE DB status constant DBSTATUS\_S\_ISNULL:</span></span>

```xml 
 
<z:row ShipperID="1"/> 
```

<span data-ttu-id="1b284-141">Si la ligne était entièrement vide, comme suit, le fournisseur de persistance retournerait l’état OLE DBSTATUS E UNAVAILABLE pour ShipperID et \_ \_ DBSTATUS S ISNULL pour \_ \_ CompanyName.</span><span class="sxs-lookup"><span data-stu-id="1b284-141">If the row was entirely empty, as follows, the Persistence Provider would return an OLE DB status of DBSTATUS\_E\_UNAVAILABLE for ShipperID and DBSTATUS\_S\_ISNULL for CompanyName.</span></span>

```xml 
 
<z:row/>  
```

<span data-ttu-id="1b284-142">Notez qu'une chaîne vide (de longueur nulle) n'équivaut pas à une chaîne de valeur Null.</span><span class="sxs-lookup"><span data-stu-id="1b284-142">Note that a zero-length string is not the same as null.</span></span>

```xml 
 
<z:row ShipperID="1" CompanyName=""/> 
```

<span data-ttu-id="1b284-143">Pour la ligne précédente, le fournisseur de persistance retourne l’état OLE DB DB DBSTATUS S OK pour les \_ \_ deux colonnes.</span><span class="sxs-lookup"><span data-stu-id="1b284-143">For the preceding row, the Persistence Provider will return an OLE DB status of DBSTATUS\_S\_OK for both columns.</span></span> <span data-ttu-id="1b284-144">Dans ce cas, la valeur de la colonne CompanyName est simplement "" (une chaîne vide).</span><span class="sxs-lookup"><span data-stu-id="1b284-144">The CompanyName in this case is simply "" (a zero-length string).</span></span>

<span data-ttu-id="1b284-145">Pour plus d'informations sur les constructions OLE DB utilisables dans le schéma d'un document XML pour OLE DB, reportez-vous à la définition de « "urn:schemas-microsoft-com:rowset » et au manuel OLE DB Programmer's Guide (en anglais).</span><span class="sxs-lookup"><span data-stu-id="1b284-145">For further information about the OLE DB constructs available for use within the schema of an XML document for OLE DB, see the definition of "urn:schemas-microsoft-com:rowset" and the OLE DB Programmer's Guide.</span></span>

