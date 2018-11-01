---
title: Section de données (référence de base de données du bureau Access)
TOCTitle: Data Section
ms:assetid: fd8d31aa-af13-a52f-5e91-20225b8df175
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250303(v=office.15)
ms:contentKeyID: 48548920
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 74406232a6f7d458eebb242f3f341bd4e3ccc583
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882853"
---
# <a name="data-section"></a><span data-ttu-id="bff1d-102">Section Données</span><span class="sxs-lookup"><span data-stu-id="bff1d-102">Data Section</span></span>

<span data-ttu-id="bff1d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bff1d-103">**Applies to**: Access 2013, Office 2013</span></span>
 
## <a name="data-section"></a><span data-ttu-id="bff1d-104">Section des données</span><span class="sxs-lookup"><span data-stu-id="bff1d-104">Data Section</span></span>

<span data-ttu-id="bff1d-p101">La section des données définit les données du groupe de lignes ainsi que toutes les mises à jour, insertions ou suppressions en attente. Elle peut contenir zéro ou plusieurs lignes. Elle peut uniquement contenir des données d'un seul groupe de lignes, la ligne étant définie par le schéma. En outre, comme mentionné précédemment, les colonnes dépourvues de données peuvent être ignorées. Si un attribut ou un sous-élément est utilisé dans la section des données et que cette construction a été définie dans la section du schéma, il est ignoré de façon silencieuse.</span><span class="sxs-lookup"><span data-stu-id="bff1d-p101">The data section defines the data of the rowset along with any pending updates, insertions, or deletions. The data section may contain zero or more rows. It may only contain data from one rowset where the row is defined by the schema. Also, as noted before, columns without any data may be omitted. If an attribute or subelement is used in the data section and that construct has not been defined in the schema section, it is silently ignored.</span></span>

## <a name="string"></a><span data-ttu-id="bff1d-110">Chaîne</span><span class="sxs-lookup"><span data-stu-id="bff1d-110">String</span></span>

<span data-ttu-id="bff1d-p102">Les caractères XML réservés dans les données texte doivent être remplacés par des entités de caractères appropriées. Par exemple, dans le nom de société « Joe's Garage », le guillemet simple doit être remplacé par une entité. La ligne doit donc ressembler à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="bff1d-p102">Reserved XML characters in text data must be replaced with appropriate character entities. For example, in the company name "Joe's Garage," the single quote character must be replaced by an entity. The actual row would look like:</span></span>

```xml  
<z:row CompanyName="Joe&apos;s Garage"/> 
```

<span data-ttu-id="bff1d-114">Les caractères suivants sont réservés dans XML et doivent être remplacés par des entités de caractères : {', », &,\<,\>}.</span><span class="sxs-lookup"><span data-stu-id="bff1d-114">The following characters are reserved in XML and must be replaced by character entities: {',",&,\<,\>}.</span></span>

## <a name="binary"></a><span data-ttu-id="bff1d-115">Binaire</span><span class="sxs-lookup"><span data-stu-id="bff1d-115">Binary</span></span>

<span data-ttu-id="bff1d-116">Les données binaires sont codées en type de données bin.hex (c'est-à-dire qu'un octet correspond à deux caractères, un caractère par quartet).</span><span class="sxs-lookup"><span data-stu-id="bff1d-116">Binary data is bin.hex encoded (that is, one byte maps to two characters, one character per nibble).</span></span>

## <a name="datetime"></a><span data-ttu-id="bff1d-117">DateTime</span><span class="sxs-lookup"><span data-stu-id="bff1d-117">DateTime</span></span>

<span data-ttu-id="bff1d-118">La variante VT\_format de DATE n’est pas directement pris en charge par les types de données XML-Data.</span><span class="sxs-lookup"><span data-stu-id="bff1d-118">The variant VT\_DATE format is not directly supported by XML-Data data types.</span></span> <span data-ttu-id="bff1d-119">Le format correct des dates avec un composant à la fois une date et l’heure est aaaa-mm-jj**T**hh.</span><span class="sxs-lookup"><span data-stu-id="bff1d-119">The correct format for dates with both a data and time component is yyyy-mm-dd**T**hh:mm:ss.</span></span>

<span data-ttu-id="bff1d-120">Pour plus d’informations sur les formats de date spécifiés par XML, consultez [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span><span class="sxs-lookup"><span data-stu-id="bff1d-120">For more information about date formats specified by XML, see [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span></span>

<span data-ttu-id="bff1d-121">Lorsque la spécification XML-Data définit deux types de données équivalents (par exemple, i4 == int), ADO écrit le nom convivial mais lit les deux formats.</span><span class="sxs-lookup"><span data-stu-id="bff1d-121">When the XML-Data specification defines two equivalent data types (for example, i4 == int), ADO will write out the friendly name but read in both.</span></span>

## <a name="managing-pending-changes"></a><span data-ttu-id="bff1d-122">Gestion des modifications en attente</span><span class="sxs-lookup"><span data-stu-id="bff1d-122">Managing Pending Changes</span></span>

<span data-ttu-id="bff1d-p104">Vous pouvez ouvrir un objet **Recordset** en mode de mise à jour immédiate ou par lot. Dans le cas d'une ouverture en mode de mise à jour par lot avec des curseurs côté client, toutes les modifications apportées à l'objet **Recordset** sont en attente tant que la méthode **UpdateBatch** n'a pas été appelée. Les modifications en attente sont aussi conservées lorsque l'objet **Recordset** est enregistré. Dans XML, elles sont représentées par l'utilisation d'éléments de mise à jour définis dans urn:schemas-microsoft-com:rowset. En outre, si un groupe de lignes peut être mis à jour, la propriété modifiable doit être affectée de la valeur True dans la définition de la ligne. Par exemple, pour indiquer que la table Shippers contient des modifications en attente, la définition de la ligne doit ressembler à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="bff1d-p104">A **Recordset** can be opened in immediate or batch update mode. When opened in batch update mode with client-side cursors, all changes made to the **Recordset** are in a pending state until the **UpdateBatch** method is called. Pending changes are also persisted when the **Recordset** is saved. In XML, they are represented by the use of the "update" elements defined in urn:schemas-microsoft-com:rowset. In addition, if a rowset can be updated, the updatable property must be set to true in the definition of the row. For example, to define that the Shippers table contains pending changes, the row definition would look like the following:</span></span>

```xml 
<s:ElementType name="row" content="eltOnly" updatable="true"> 
  <s:attribute type="ShipperID"/> 
  <s:attribute type="CompanyName"/> 
  <s:attribute type="Phone"/> 
  <s:extends type="rs:rowbase"/> 
</s:ElementType> 
```

<span data-ttu-id="bff1d-129">Ceci indique au fournisseur de persistance d'exposer les données afin qu'ADO puisse créer un objet **Recordset** modifiable.</span><span class="sxs-lookup"><span data-stu-id="bff1d-129">This tells the Persistence Provider to surface data so that ADO can construct an updatable **Recordset** object.</span></span>

<span data-ttu-id="bff1d-130">L'exemple de données suivant montre à quoi ressemblent les insertions, modifications et suppressions dans le fichier persisté :</span><span class="sxs-lookup"><span data-stu-id="bff1d-130">The following sample data shows how insertions, changes, and deletions look in the persisted file:</span></span>

```xml 
<rs:data> 
  <z:row ShipperID="2" CompanyName="United Package"  
    Phone="(503) 555-3199"/> 
<rs:update> 
  <rs:original> 
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/> 
  </rs:original> 
  <z:row Phone="(503) 552-7134"/> 
</rs:update> 
<rs:insert> 
  <z:row ShipperID="12" CompanyName="Lightning Shipping"  
    Phone="(505) 111-2222"/> 
  <z:row ShipperID="13" CompanyName="Thunder Overnight"  
    Phone="(505) 111-2222"/> 
  <z:row ShipperID="14" CompanyName="Blue Angel Air Delivery"  
    Phone="(505) 111-2222"/> 
</rs:insert> 
<rs:delete> 
  <z:row ShipperID="1" CompanyName="Speedy Express" Phone="(503) 555-9831"/> 
</rs:delete> 
</rs:data> 
```

<span data-ttu-id="bff1d-p105">Une mise à jour contient toujours les données de la ligne source complète suivies des données de la ligne modifiée. La ligne modifiée peut contenir toutes les colonnes ou seulement celles qui ont été modifiées. Dans l'exemple précédent, la ligne relative à Shipper 2 n'a pas été modifiée tandis que seule la colonne Phone l'a été pour Shipper 3 et est donc la seule colonne comprise dans la ligne modifiée. Les lignes insérées pour Shipper 12, 13 et 14 sont regroupées sous une seule balise rs:insert. Notez que les lignes supprimées peuvent être aussi regroupées, bien que l'exemple ne le montre pas.</span><span class="sxs-lookup"><span data-stu-id="bff1d-p105">An update always contains the entire original row data followed by the changed row data. The changed row may contain all of the columns or only those columns that have actually changed. In the previous example, the row for Shipper 2 is not changed, while only the Phone column has changed values for Shipper 3 and is therefore the only column included in the changed row. The inserted rows for Shippers 12, 13, and 14 are batched together under one rs:insert tag. Note that deleted rows may also be batched together, although this is not shown above.</span></span>

