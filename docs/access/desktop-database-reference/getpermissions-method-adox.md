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
# <a name="getpermissions-method-adox"></a><span data-ttu-id="61711-102">GetPermissions, méthode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="61711-102">GetPermissions method (ADOX)</span></span>

<span data-ttu-id="61711-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="61711-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="61711-104">Renvoie les autorisations d'un groupe ou d'un utilisateur sur un objet ou un conteneur d'objets.</span><span class="sxs-lookup"><span data-stu-id="61711-104">Returns the permissions for a group or user on an object or object container.</span></span>

## <a name="syntax"></a><span data-ttu-id="61711-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61711-105">Syntax</span></span>

<span data-ttu-id="61711-106">*ReturnValue*  =  *GroupOrUser*. GetPermissions(*Name*, *ObjectType* \[ ,*ObjectTypeId* \] )</span><span class="sxs-lookup"><span data-stu-id="61711-106">*ReturnValue* = *GroupOrUser*.GetPermissions(*Name*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="61711-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="61711-107">Return value</span></span>

<span data-ttu-id="61711-p101">Renvoie une valeur de type **Long** qui spécifie un masque de bits contenant les autorisations que le groupe ou l'utilisateur ont sur l'objet. Cette valeur peut correspondre à une ou plusieurs constantes [RightsEnum](rightsenum.md).</span><span class="sxs-lookup"><span data-stu-id="61711-p101">Returns a **Long** value that specifies a bitmask containing the permissions that the group or user has on the object. This value can be one or more of the [RightsEnum](rightsenum.md) constants.</span></span>

## <a name="parameters"></a><span data-ttu-id="61711-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61711-110">Parameters</span></span>

|<span data-ttu-id="61711-111">Paramètre</span><span class="sxs-lookup"><span data-stu-id="61711-111">Parameter</span></span>|<span data-ttu-id="61711-112">Description</span><span class="sxs-lookup"><span data-stu-id="61711-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="61711-113">*Name*</span><span class="sxs-lookup"><span data-stu-id="61711-113">*Name*</span></span> |<span data-ttu-id="61711-p102">Valeur de type **Variant** qui spécifie le nom de l'objet dont il faut définir les autorisations. Attribuez une valeur Null au paramètre *Name* pour obtenir des autorisations pour le conteneur d'objets.</span><span class="sxs-lookup"><span data-stu-id="61711-p102">A **Variant** value that specifies the name of the object for which to set permissions. Set *Name* to a null value if you want to get the permissions for the object container.</span></span>|
|<span data-ttu-id="61711-116">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="61711-116">*ObjectType*</span></span> |<span data-ttu-id="61711-117">Valeur de type **Long** qui peut être l'une des constantes [ObjectTypeEnum](objecttypeenum.md), spécifiant le type d'objet dont il faut obtenir les autorisations.</span><span class="sxs-lookup"><span data-stu-id="61711-117">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="61711-118">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="61711-118">*ObjectTypeId*</span></span> |<span data-ttu-id="61711-p103">Facultatif. Valeur de type **Variant** qui spécifie le GUID d'un type d'objet fournisseur non défini par la spécification OLE DB. Ce paramètre est requis si *ObjectType* a la valeur **adPermObjProviderSpecific**. Sinon, il n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="61711-p103">Optional. A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification. This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

