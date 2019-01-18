---
title: GetPermissions, méthode (ADOX)
TOCTitle: GetPermissions method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa5dda3c8e2ee8251fc54f4ff3bc12be0aca5002
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719742"
---
# <a name="getpermissions-method-adox"></a>GetPermissions, méthode (ADOX)

**S’applique à**: Access 2013, Office 2013

Renvoie les autorisations d'un groupe ou d'un utilisateur sur un objet ou un conteneur d'objets.

## <a name="syntax"></a>Syntaxe

*Valeur False* = *Groupe_ou_utilisateur*. GetPermissions (*nom*, *ObjectType* \[,*ObjectTypeId*\])

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur de type **Long** qui spécifie un masque de bits contenant les autorisations que le groupe ou l'utilisateur ont sur l'objet. Cette valeur peut correspondre à une ou plusieurs constantes [RightsEnum](rightsenum.md).

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Name* |Valeur de type **Variant** qui spécifie le nom de l'objet dont il faut définir les autorisations. Définir le *nom* à une valeur null si vous souhaitez obtenir des autorisations pour le conteneur d’objet.|
|*ObjectType* |Valeur de type **Long** qui peut être l'une des constantes [ObjectTypeEnum](objecttypeenum.md), spécifiant le type d'objet dont il faut obtenir les autorisations.|
|*ObjectTypeId* |Facultatif. Une valeur de **type Variant** qui spécifie le GUID pour un type d’objet fournisseur non défini par la spécification OLE DB. Ce paramètre est requis si *ObjectType* a la valeur **adPermObjProviderSpecific**. dans le cas contraire, il n’est pas utilisé.|

