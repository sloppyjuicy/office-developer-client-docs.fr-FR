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
# <a name="data-section"></a>Section Données

**S’applique à**: Access 2013, Office 2013
 
## <a name="data-section"></a>Section des données

La section des données définit les données du groupe de lignes ainsi que toutes les mises à jour, insertions ou suppressions en attente. Elle peut contenir zéro ou plusieurs lignes. Elle peut uniquement contenir des données d'un seul groupe de lignes, la ligne étant définie par le schéma. En outre, comme mentionné précédemment, les colonnes dépourvues de données peuvent être ignorées. Si un attribut ou un sous-élément est utilisé dans la section des données et que cette construction a été définie dans la section du schéma, il est ignoré de façon silencieuse.

## <a name="string"></a>Chaîne

Les caractères XML réservés dans les données texte doivent être remplacés par des entités de caractères appropriées. Par exemple, dans le nom de société « Joe's Garage », le guillemet simple doit être remplacé par une entité. La ligne doit donc ressembler à ce qui suit :

```xml  
<z:row CompanyName="Joe&apos;s Garage"/> 
```

Les caractères suivants sont réservés dans XML et doivent être remplacés par des entités de caractères : {', », &,\<,\>}.

## <a name="binary"></a>Binaire

Les données binaires sont codées en type de données bin.hex (c'est-à-dire qu'un octet correspond à deux caractères, un caractère par quartet).

## <a name="datetime"></a>DateTime

La variante VT\_format de DATE n’est pas directement pris en charge par les types de données XML-Data. Le format correct des dates avec un composant à la fois une date et l’heure est aaaa-mm-jj**T**hh.

Pour plus d’informations sur les formats de date spécifiés par XML, consultez [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).

Lorsque la spécification XML-Data définit deux types de données équivalents (par exemple, i4 == int), ADO écrit le nom convivial mais lit les deux formats.

## <a name="managing-pending-changes"></a>Gestion des modifications en attente

Vous pouvez ouvrir un objet **Recordset** en mode de mise à jour immédiate ou par lot. Dans le cas d'une ouverture en mode de mise à jour par lot avec des curseurs côté client, toutes les modifications apportées à l'objet **Recordset** sont en attente tant que la méthode **UpdateBatch** n'a pas été appelée. Les modifications en attente sont aussi conservées lorsque l'objet **Recordset** est enregistré. Dans XML, elles sont représentées par l'utilisation d'éléments de mise à jour définis dans urn:schemas-microsoft-com:rowset. En outre, si un groupe de lignes peut être mis à jour, la propriété modifiable doit être affectée de la valeur True dans la définition de la ligne. Par exemple, pour indiquer que la table Shippers contient des modifications en attente, la définition de la ligne doit ressembler à ce qui suit :

```xml 
<s:ElementType name="row" content="eltOnly" updatable="true"> 
  <s:attribute type="ShipperID"/> 
  <s:attribute type="CompanyName"/> 
  <s:attribute type="Phone"/> 
  <s:extends type="rs:rowbase"/> 
</s:ElementType> 
```

Ceci indique au fournisseur de persistance d'exposer les données afin qu'ADO puisse créer un objet **Recordset** modifiable.

L'exemple de données suivant montre à quoi ressemblent les insertions, modifications et suppressions dans le fichier persisté :

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

Une mise à jour contient toujours les données de la ligne source complète suivies des données de la ligne modifiée. La ligne modifiée peut contenir toutes les colonnes ou seulement celles qui ont été modifiées. Dans l'exemple précédent, la ligne relative à Shipper 2 n'a pas été modifiée tandis que seule la colonne Phone l'a été pour Shipper 3 et est donc la seule colonne comprise dans la ligne modifiée. Les lignes insérées pour Shipper 12, 13 et 14 sont regroupées sous une seule balise rs:insert. Notez que les lignes supprimées peuvent être aussi regroupées, bien que l'exemple ne le montre pas.

