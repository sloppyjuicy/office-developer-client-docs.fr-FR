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
# <a name="getpermissions-method-adox"></a><span data-ttu-id="7cb67-102">GetPermissions, méthode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="7cb67-102">GetPermissions method (ADOX)</span></span>

<span data-ttu-id="7cb67-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7cb67-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7cb67-104">Renvoie les autorisations d'un groupe ou d'un utilisateur sur un objet ou un conteneur d'objets.</span><span class="sxs-lookup"><span data-stu-id="7cb67-104">Returns the permissions for a group or user on an object or object container.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cb67-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cb67-105">Syntax</span></span>

<span data-ttu-id="7cb67-106">*Valeur False* = *Groupe_ou_utilisateur*. GetPermissions (*nom*, *ObjectType* \[,*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="7cb67-106">*ReturnValue* = *GroupOrUser*.GetPermissions(*Name*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="7cb67-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7cb67-107">Return value</span></span>

<span data-ttu-id="7cb67-p101">Renvoie une valeur de type **Long** qui spécifie un masque de bits contenant les autorisations que le groupe ou l'utilisateur ont sur l'objet. Cette valeur peut correspondre à une ou plusieurs constantes [RightsEnum](rightsenum.md).</span><span class="sxs-lookup"><span data-stu-id="7cb67-p101">Returns a **Long** value that specifies a bitmask containing the permissions that the group or user has on the object. This value can be one or more of the [RightsEnum](rightsenum.md) constants.</span></span>

## <a name="parameters"></a><span data-ttu-id="7cb67-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cb67-110">Parameters</span></span>

|<span data-ttu-id="7cb67-111">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7cb67-111">Parameter</span></span>|<span data-ttu-id="7cb67-112">Description</span><span class="sxs-lookup"><span data-stu-id="7cb67-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="7cb67-113">*Name*</span><span class="sxs-lookup"><span data-stu-id="7cb67-113">*Name*</span></span> |<span data-ttu-id="7cb67-114">Valeur de type **Variant** qui spécifie le nom de l'objet dont il faut définir les autorisations.</span><span class="sxs-lookup"><span data-stu-id="7cb67-114">A **Variant** value that specifies the name of the object for which to set permissions.</span></span> <span data-ttu-id="7cb67-115">Définir le *nom* à une valeur null si vous souhaitez obtenir des autorisations pour le conteneur d’objet.</span><span class="sxs-lookup"><span data-stu-id="7cb67-115">Set *Name* to a null value if you want to get the permissions for the object container.</span></span>|
|<span data-ttu-id="7cb67-116">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="7cb67-116">*ObjectType*</span></span> |<span data-ttu-id="7cb67-117">Valeur de type **Long** qui peut être l'une des constantes [ObjectTypeEnum](objecttypeenum.md), spécifiant le type d'objet dont il faut obtenir les autorisations.</span><span class="sxs-lookup"><span data-stu-id="7cb67-117">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="7cb67-118">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="7cb67-118">*ObjectTypeId*</span></span> |<span data-ttu-id="7cb67-119">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="7cb67-119">Optional.</span></span> <span data-ttu-id="7cb67-120">Une valeur de **type Variant** qui spécifie le GUID pour un type d’objet fournisseur non défini par la spécification OLE DB.</span><span class="sxs-lookup"><span data-stu-id="7cb67-120">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="7cb67-121">Ce paramètre est requis si *ObjectType* a la valeur **adPermObjProviderSpecific**. dans le cas contraire, il n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="7cb67-121">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

