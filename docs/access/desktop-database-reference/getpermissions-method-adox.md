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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292243"
---
# <a name="getpermissions-method-adox"></a>GetPermissions, méthode (ADOX)

**S’applique à** : Access 2013, Office 2013

Renvoie les autorisations d'un groupe ou d'un utilisateur sur un objet ou un conteneur d'objets.

## <a name="syntax"></a>Syntaxe

*ReturnValue*  =  *GroupOrUser*. GetPermissions(*Name*, *ObjectType* \[ ,*ObjectTypeId* \] )

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur de type **Long** qui spécifie un masque de bits contenant les autorisations que le groupe ou l'utilisateur ont sur l'objet. Cette valeur peut correspondre à une ou plusieurs constantes [RightsEnum](rightsenum.md).

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Name* |Valeur de type **Variant** qui spécifie le nom de l'objet dont il faut définir les autorisations. Attribuez une valeur Null au paramètre *Name* pour obtenir des autorisations pour le conteneur d'objets.|
|*ObjectType* |Valeur de type **Long** qui peut être l'une des constantes [ObjectTypeEnum](objecttypeenum.md), spécifiant le type d'objet dont il faut obtenir les autorisations.|
|*ObjectTypeId* |Facultatif. Valeur de type **Variant** qui spécifie le GUID d'un type d'objet fournisseur non défini par la spécification OLE DB. Ce paramètre est requis si *ObjectType* a la valeur **adPermObjProviderSpecific**. Sinon, il n'est pas utilisé.|

