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
# <a name="setpermissions-method-adox"></a><span data-ttu-id="69808-102">SetPermissions, méthode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="69808-102">SetPermissions method (ADOX)</span></span>

<span data-ttu-id="69808-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69808-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69808-104">Spécifie les autorisations d'un groupe ou d'un utilisateur sur un objet.</span><span class="sxs-lookup"><span data-stu-id="69808-104">Specifies the permissions for a group or user on an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="69808-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69808-105">Syntax</span></span>

<span data-ttu-id="69808-106">*GroupOrUser*. SetPermissions *Name*, *ObjectType*, *Action*, *Rights* \[ ,*Inherit* \] \[ ,*ObjectTypeId*\]</span><span class="sxs-lookup"><span data-stu-id="69808-106">*GroupOrUser*.SetPermissions *Name*, *ObjectType*, *Action*, *Rights* \[,*Inherit*\] \[,*ObjectTypeId*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="69808-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69808-107">Parameters</span></span>

|<span data-ttu-id="69808-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="69808-108">Parameter</span></span>|<span data-ttu-id="69808-109">Description</span><span class="sxs-lookup"><span data-stu-id="69808-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="69808-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="69808-110">*Name*</span></span> |<span data-ttu-id="69808-111">Valeur de type **String** qui spécifie le nom de l'objet dont il faut définir les autorisations.</span><span class="sxs-lookup"><span data-stu-id="69808-111">A **String** value that specifies the name of the object for which to set permissions.</span></span>|
|<span data-ttu-id="69808-112">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="69808-112">*ObjectType*</span></span> |<span data-ttu-id="69808-113">Valeur de type **Long** qui peut être l'une des constantes [ObjectTypeEnum](objecttypeenum.md), spécifiant le type d'objet dont il faut obtenir les autorisations.</span><span class="sxs-lookup"><span data-stu-id="69808-113">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="69808-114">*Action*</span><span class="sxs-lookup"><span data-stu-id="69808-114">*Action*</span></span> |<span data-ttu-id="69808-115">Valeur de type **Long** qui peut correspondre à l'une des constantes [ActionEnum](actionenum.md), spécifiant le type d'action à effectuer lors de la configuration des autorisations.</span><span class="sxs-lookup"><span data-stu-id="69808-115">A **Long** value which can be one of the [ActionEnum](actionenum.md) constants that specifies the type of action to perform when setting permissions.</span></span>|
|<span data-ttu-id="69808-116">*Rights*</span><span class="sxs-lookup"><span data-stu-id="69808-116">*Rights*</span></span> |<span data-ttu-id="69808-117">Valeur de type **Long** qui peut être un masque de bits d'une ou plusieurs constantes [RightsEnum](rightsenum.md), indiquant les droits à définir.</span><span class="sxs-lookup"><span data-stu-id="69808-117">A **Long** value which can be a bitmask of one or more of the [RightsEnum](rightsenum.md) constants, that indicates the rights to set.</span></span>|
|<span data-ttu-id="69808-118">*Inherit*</span><span class="sxs-lookup"><span data-stu-id="69808-118">*Inherit*</span></span> |<span data-ttu-id="69808-p101">Facultatif. Valeur de type **Long** qui peut correspondre à l'une des constantes [InheritTypeEnum](inherittypeenum.md), qui spécifie la manière dont les objets héritent des autorisations. La valeur par défaut est **adInheritNone**.</span><span class="sxs-lookup"><span data-stu-id="69808-p101">Optional. A **Long** value which can be one of the [InheritTypeEnum](inherittypeenum.md) constants, that specifies how objects will inherit these permissions. The default value is **adInheritNone**.</span></span>|
|<span data-ttu-id="69808-122">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="69808-122">*ObjectTypeId*</span></span> |<span data-ttu-id="69808-p102">Facultatif. Valeur de type **Variant** qui spécifie le GUID d'un type d'objet fournisseur non défini par la spécification OLE DB. Ce paramètre est requis si *ObjectType* a la valeur **adPermObjProviderSpecific**. Sinon, il n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="69808-p102">Optional. A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification. This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="69808-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="69808-126">Remarks</span></span>

<span data-ttu-id="69808-127">Une erreur se produit si le fournisseur ne prend pas en charge la définition de droits d'accès pour les groupes ou utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="69808-127">An error will occur if the provider does not support setting access rights for groups or users.</span></span>

> [!NOTE]
> <span data-ttu-id="69808-p103">En cas d'appel de **SetPermissions**, l'octroi de la valeur **adAccessRevoke** au paramètre Actions remplace la configuration du paramètre *Rights*. N'affectez pas la valeur **adAccessRevoke** au paramètre *Actions* si vous souhaitez que les droits spécifiés dans le paramètre *Rights* soient appliqués.</span><span class="sxs-lookup"><span data-stu-id="69808-p103">When calling **SetPermissions**, setting Actions to **adAccessRevoke** overrides any settings of the *Rights* parameter. Do not set *Actions* to **adAccessRevoke** if you want the rights specified in the *Rights* parameter to take effect.</span></span>


