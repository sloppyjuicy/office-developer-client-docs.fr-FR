---
title: SortOrder, propriété (ADOX)
TOCTitle: SortOrder property (ADOX)
ms:assetid: c2b8c84d-acc4-9929-fff5-9a088abbfcf1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249951(v=office.15)
ms:contentKeyID: 48547557
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ee094166e971a321d0a775fcfd8d841bfb0fc047
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919632"
---
# <a name="sortorder-property-adox"></a>SortOrder, propriété (ADOX)


**S’applique à**: Access 2013, Office 2013

Spécifie la séquence de tri pour la colonne (colonnes d'index uniquement).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit et renvoie une valeur de type **Long** qui peut correspondre à l'une des constantes [SortOrderEnum](sortorderenum.md). La valeur par défaut est **adSortAscending**.

## <a name="remarks"></a>Notes

Cette propriété s'applique uniquement aux objets [Column](column-object-adox.md)de la collection [Columns](columns-collection-adox.md) d'un objet [Index](index-object-adox.md).

