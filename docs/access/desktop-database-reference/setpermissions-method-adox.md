---
title: SetPermissions, méthode (ADOX)
TOCTitle: SetPermissions method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f9b393e90d579c131865b112263efd0aef3216b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314580"
---
# <a name="setpermissions-method-adox"></a>SetPermissions, méthode (ADOX)

**S’applique à** : Access 2013, Office 2013

Spécifie les autorisations d'un groupe ou d'un utilisateur sur un objet.

## <a name="syntax"></a>Syntaxe

*GroupOrUser*. SetPermissions *Name*, *ObjectType*, *Action*, *Rights* \[ ,*Inherit* \] \[ ,*ObjectTypeId*\]

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Name* |Valeur de type **String** qui spécifie le nom de l'objet dont il faut définir les autorisations.|
|*ObjectType* |Valeur de type **Long** qui peut être l'une des constantes [ObjectTypeEnum](objecttypeenum.md), spécifiant le type d'objet dont il faut obtenir les autorisations.|
|*Action* |Valeur de type **Long** qui peut correspondre à l'une des constantes [ActionEnum](actionenum.md), spécifiant le type d'action à effectuer lors de la configuration des autorisations.|
|*Rights* |Valeur de type **Long** qui peut être un masque de bits d'une ou plusieurs constantes [RightsEnum](rightsenum.md), indiquant les droits à définir.|
|*Inherit* |Facultatif. Valeur de type **Long** qui peut correspondre à l'une des constantes [InheritTypeEnum](inherittypeenum.md), qui spécifie la manière dont les objets héritent des autorisations. La valeur par défaut est **adInheritNone**.|
|*ObjectTypeId* |Facultatif. Valeur de type **Variant** qui spécifie le GUID d'un type d'objet fournisseur non défini par la spécification OLE DB. Ce paramètre est requis si *ObjectType* a la valeur **adPermObjProviderSpecific**. Sinon, il n'est pas utilisé.|

## <a name="remarks"></a>Remarques

Une erreur se produit si le fournisseur ne prend pas en charge la définition de droits d'accès pour les groupes ou utilisateurs.

> [!NOTE]
> En cas d'appel de **SetPermissions**, l'octroi de la valeur **adAccessRevoke** au paramètre Actions remplace la configuration du paramètre *Rights*. N'affectez pas la valeur **adAccessRevoke** au paramètre *Actions* si vous souhaitez que les droits spécifiés dans le paramètre *Rights* soient appliqués.


