---
title: GetPermissions, méthode (ADOX)
TOCTitle: GetPermissions Method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b7e6603d8da5bafc7a479cb8bfe94577a0679bd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471543"
---
# <a name="getpermissions-method-adox"></a><span data-ttu-id="06482-102">GetPermissions, méthode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="06482-102">GetPermissions Method (ADOX)</span></span>


<span data-ttu-id="06482-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="06482-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="06482-104">Renvoie les autorisations d'un groupe ou d'un utilisateur sur un objet ou un conteneur d'objets.</span><span class="sxs-lookup"><span data-stu-id="06482-104">Returns the permissions for a group or user on an object or object container.</span></span>

## <a name="syntax"></a><span data-ttu-id="06482-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06482-105">Syntax</span></span>

<span data-ttu-id="06482-106">*Valeur False* = *Groupe_ou_utilisateur*. GetPermissions (*nom*, *ObjectType* \[,*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="06482-106">*ReturnValue* = *GroupOrUser*.GetPermissions(*Name*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="06482-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="06482-107">Return Value</span></span>

<span data-ttu-id="06482-p101">Renvoie une valeur de type **Long** qui spécifie un masque de bits contenant les autorisations que le groupe ou l'utilisateur ont sur l'objet. Cette valeur peut correspondre à une ou plusieurs constantes [RightsEnum](rightsenum.md).</span><span class="sxs-lookup"><span data-stu-id="06482-p101">Returns a **Long** value that specifies a bitmask containing the permissions that the group or user has on the object. This value can be one or more of the [RightsEnum](rightsenum.md) constants.</span></span>

## <a name="parameters"></a><span data-ttu-id="06482-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06482-110">Parameters</span></span>

  - <span data-ttu-id="06482-111">*Name*</span><span class="sxs-lookup"><span data-stu-id="06482-111">*Name*</span></span>

  - <span data-ttu-id="06482-112">Valeur de type **Variant** qui spécifie le nom de l'objet dont il faut définir les autorisations.</span><span class="sxs-lookup"><span data-stu-id="06482-112">A **Variant** value that specifies the name of the object for which to set permissions.</span></span> <span data-ttu-id="06482-113">Définir le *nom* à une valeur null si vous souhaitez obtenir des autorisations pour le conteneur d’objet.</span><span class="sxs-lookup"><span data-stu-id="06482-113">Set *Name* to a null value if you want to get the permissions for the object container.</span></span>

  - <span data-ttu-id="06482-114">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="06482-114">*ObjectType*</span></span>

  - <span data-ttu-id="06482-115">Valeur de type **Long** qui peut être l'une des constantes [ObjectTypeEnum](objecttypeenum.md), spécifiant le type d'objet dont il faut obtenir les autorisations.</span><span class="sxs-lookup"><span data-stu-id="06482-115">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>

  - <span data-ttu-id="06482-116">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="06482-116">*ObjectTypeId*</span></span>

  - <span data-ttu-id="06482-117">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="06482-117">Optional.</span></span> <span data-ttu-id="06482-118">Une valeur de **type Variant** qui spécifie le GUID pour un type d’objet fournisseur non défini par la spécification OLE DB.</span><span class="sxs-lookup"><span data-stu-id="06482-118">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="06482-119">Ce paramètre est requis si *ObjectType* a la valeur **adPermObjProviderSpecific**. dans le cas contraire, il n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="06482-119">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

