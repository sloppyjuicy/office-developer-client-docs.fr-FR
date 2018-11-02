---
title: GetObjectOwner, méthode (ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b1a37b0f341c849358b649c2222df2955fd88f5d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927811"
---
# <a name="getobjectowner-method-adox"></a>GetObjectOwner, méthode (ADOX)


**S’applique à**: Access 2013, Office 2013


Renvoie le propriétaire d'un objet dans un objet [Catalog](catalog-object-adox.md).

## <a name="syntax"></a>Syntaxe

*Propriétaire* = *catalogue*. GetObjectOwner (*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur de type **String** qui spécifie la propriété [Name](name-property-adox.md) de l'objet [User](user-object-adox.md) ou [Group](group-object-adox.md) qui détient l'objet.

## <a name="parameters"></a>Paramètres

  - *ObjectName*

  - Valeur de type **String** qui spécifie le nom de l'objet dont le propriétaire doit être renvoyé.

  - *ObjectType*

  - Valeur de type **Long** qui peut être l'une des constantes [ObjectTypeEnum](objecttypeenum.md), spécifiant le type d'objet dont il faut obtenir le propriétaire.

  - *ObjectTypeId*

  - Facultatif. Une valeur de **type Variant** qui spécifie le GUID pour un type d’objet fournisseur non défini par la spécification OLE DB. Ce paramètre est requis si *ObjectType* a la valeur **adPermObjProviderSpecific**. dans le cas contraire, il n’est pas utilisé.

## <a name="remarks"></a>Notes

Une erreur se produit si le fournisseur ne prend pas en charge le renvoi des propriétaires d'objets.

