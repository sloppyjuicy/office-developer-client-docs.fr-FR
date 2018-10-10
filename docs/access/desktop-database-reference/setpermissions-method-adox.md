---
title: SetPermissions, méthode (ADOX)
TOCTitle: SetPermissions Method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35578de28509e510e9ba5329cfdabc2eff8207b1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471566"
---
# <a name="setpermissions-method-adox"></a><span data-ttu-id="bf1bd-102">SetPermissions, méthode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="bf1bd-102">SetPermissions Method (ADOX)</span></span>


<span data-ttu-id="bf1bd-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf1bd-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="bf1bd-104">Spécifie les autorisations d'un groupe ou d'un utilisateur sur un objet.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-104">Specifies the permissions for a group or user on an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf1bd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf1bd-105">Syntax</span></span>

<span data-ttu-id="bf1bd-106">*Groupe_ou_utilisateur*. SetPermissions*nom*, *ObjectType*, *Action*, *droits* \[,*hériter* \] \[,*ObjectTypeId*\]</span><span class="sxs-lookup"><span data-stu-id="bf1bd-106">*GroupOrUser*.SetPermissions*Name*, *ObjectType*, *Action*, *Rights* \[,*Inherit*\] \[,*ObjectTypeId*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="bf1bd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf1bd-107">Parameters</span></span>

  - <span data-ttu-id="bf1bd-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="bf1bd-108">*Name*</span></span>

  - <span data-ttu-id="bf1bd-109">Valeur de type **String** qui spécifie le nom de l'objet dont il faut définir les autorisations.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-109">A **String** value that specifies the name of the object for which to set permissions.</span></span>

  - <span data-ttu-id="bf1bd-110">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="bf1bd-110">*ObjectType*</span></span>

  - <span data-ttu-id="bf1bd-111">Valeur de type **Long** qui peut être l'une des constantes [ObjectTypeEnum](objecttypeenum.md), spécifiant le type d'objet dont il faut obtenir les autorisations.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-111">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>

  - <span data-ttu-id="bf1bd-112">*Action*</span><span class="sxs-lookup"><span data-stu-id="bf1bd-112">*Action*</span></span>

  - <span data-ttu-id="bf1bd-113">Valeur de type **Long** qui peut correspondre à l'une des constantes [ActionEnum](actionenum.md), spécifiant le type d'action à effectuer lors de la configuration des autorisations.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-113">A **Long** value which can be one of the [ActionEnum](actionenum.md) constants that specifies the type of action to perform when setting permissions.</span></span>

  - <span data-ttu-id="bf1bd-114">*Rights*</span><span class="sxs-lookup"><span data-stu-id="bf1bd-114">*Rights*</span></span>

  - <span data-ttu-id="bf1bd-115">Valeur de type **Long** qui peut être un masque de bits d'une ou plusieurs constantes [RightsEnum](rightsenum.md), indiquant les droits à définir.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-115">A **Long** value which can be a bitmask of one or more of the [RightsEnum](rightsenum.md) constants, that indicates the rights to set.</span></span>

  - <span data-ttu-id="bf1bd-116">*Inherit*</span><span class="sxs-lookup"><span data-stu-id="bf1bd-116">*Inherit*</span></span>

  - <span data-ttu-id="bf1bd-p101">Facultatif. Valeur de type **Long** qui peut correspondre à l'une des constantes [InheritTypeEnum](inherittypeenum.md), qui spécifie la manière dont les objets héritent des autorisations. La valeur par défaut est **adInheritNone**.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-p101">Optional. A **Long** value which can be one of the [InheritTypeEnum](inherittypeenum.md) constants, that specifies how objects will inherit these permissions. The default value is **adInheritNone**.</span></span>

  - <span data-ttu-id="bf1bd-120">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="bf1bd-120">*ObjectTypeId*</span></span>

  - <span data-ttu-id="bf1bd-121">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-121">Optional.</span></span> <span data-ttu-id="bf1bd-122">Une valeur de **type Variant** qui spécifie le GUID pour un type d’objet fournisseur non défini par la spécification OLE DB.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-122">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="bf1bd-123">Ce paramètre est requis si *ObjectType* a la valeur **adPermObjProviderSpecific**. dans le cas contraire, il n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-123">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf1bd-124">Notes</span><span class="sxs-lookup"><span data-stu-id="bf1bd-124">Remarks</span></span>

<span data-ttu-id="bf1bd-125">Une erreur se produit si le fournisseur ne prend pas en charge la définition de droits d'accès pour les groupes ou utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-125">An error will occur if the provider does not support setting access rights for groups or users.</span></span>


> [!NOTE]
> <P><span data-ttu-id="bf1bd-126">Lorsque vous appelez la <STRONG>méthode SetPermissions</STRONG>, la définition des Actions à <STRONG>adAccessRevoke</STRONG> remplace tous les paramètres du paramètre <EM>droits</EM> .</span><span class="sxs-lookup"><span data-stu-id="bf1bd-126">When calling <STRONG>SetPermissions</STRONG>, setting Actions to <STRONG>adAccessRevoke</STRONG> overrides any settings of the <EM>Rights</EM> parameter.</span></span> <span data-ttu-id="bf1bd-127">Ne définissez pas les <EM>Actions</EM> à <STRONG>adAccessRevoke</STRONG> si vous souhaitez que les droits spécifiés dans le paramètre <EM>Rights</EM> prenne effet.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-127">Do not set <EM>Actions</EM> to <STRONG>adAccessRevoke</STRONG> if you want the rights specified in the <EM>Rights</EM> parameter to take effect.</span></span></P>


