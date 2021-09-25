---
title: GetObjectOwner, méthode (ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 215546377e085dfb1385b2f00ed882b9d3e85179
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568963"
---
# <a name="getobjectowner-method-adox"></a>GetObjectOwner, méthode (ADOX)

**S’applique à** : Access 2013, Office 2013

Renvoie le propriétaire d’un objet dans un objet [Catalog](catalog-object-adox.md).

## <a name="syntax"></a>Syntaxe

*Propriétaire*  =  *Catalogue*. GetObjectOwner(*ObjectName*, *ObjectType* \[ ,*ObjectTypeId* \] )

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur de type **String** qui spécifie la propriété [Name](name-property-adox.md) de l’objet [User](user-object-adox.md) ou [Group](group-object-adox.md) qui détient l’objet.

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*ObjectName* |Valeur de type **String** qui spécifie le nom de l'objet dont le propriétaire doit être renvoyé.|
|*ObjectType* |Valeur de type **Long** qui peut être l'une des constantes [ObjectTypeEnum](objecttypeenum.md), spécifiant le type d'objet dont il faut obtenir le propriétaire.|
|*ObjectTypeId* |Facultatif. Valeur de type **Variant** qui spécifie le GUID d'un type d'objet fournisseur non défini par la spécification OLE DB. Ce paramètre est requis si *ObjectType* a la valeur **adPermObjProviderSpecific**. Sinon, il n'est pas utilisé.|

## <a name="remarks"></a>Remarques

Une erreur se produit si le fournisseur ne prend pas en charge le renvoi des propriétaires d'objets.

