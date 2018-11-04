---
title: Méthode Stat - ActiveX Data Objects (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3853c42fab9de9e06691ae0e8efe20e23c410121
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949291"
---
# <a name="stat-method-ado"></a><span data-ttu-id="39c37-102">Stat, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="39c37-102">Stat method (ADO)</span></span>

<span data-ttu-id="39c37-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39c37-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39c37-104">Extrait des informations relatives à un objet **Stream**.</span><span class="sxs-lookup"><span data-stu-id="39c37-104">Retrieves information about a **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="39c37-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39c37-105">Syntax</span></span>

<span data-ttu-id="39c37-106">Longueur du *flux*. Stat (*StatStg*, *StatFlag*)</span><span class="sxs-lookup"><span data-stu-id="39c37-106">Long *stream*.Stat(*StatStg*, *StatFlag*)</span></span>

## <a name="return-value"></a><span data-ttu-id="39c37-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="39c37-107">Return value</span></span>

<span data-ttu-id="39c37-108">Valeur de type Long indiquant l'état de l'opération.</span><span class="sxs-lookup"><span data-stu-id="39c37-108">A long value indicating the status of the operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="39c37-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39c37-109">Parameters</span></span>

|<span data-ttu-id="39c37-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="39c37-110">Parameter</span></span>|<span data-ttu-id="39c37-111">Description</span><span class="sxs-lookup"><span data-stu-id="39c37-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="39c37-112">*StatStg*</span><span class="sxs-lookup"><span data-stu-id="39c37-112">*StatStg*</span></span> |<span data-ttu-id="39c37-p101">Structure STATSTG contenant des informations relatives au flux. L'implémentation de la méthode Stat utilisée par l'objet Stream ADO ne remplit pas tous les champs de la structure.</span><span class="sxs-lookup"><span data-stu-id="39c37-p101">A STATSTG structure that will be filled in with information about the stream. The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.</span></span>|
|<span data-ttu-id="39c37-115">*StatFlag*</span><span class="sxs-lookup"><span data-stu-id="39c37-115">*StatFlag*</span></span> |<span data-ttu-id="39c37-p102">Indique que cette méthode ne renvoie pas certains membres dans la structure STATSTG, ce qui permet d'éviter une opération d'allocation de mémoire. Les valeurs sont extraites de l'énumération STATFLAG.</span><span class="sxs-lookup"><span data-stu-id="39c37-p102">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation. Values are taken from the STATFLAG enumeration.</span></span><br/><br/><span data-ttu-id="39c37-118">L’énumération STATFLAG possède deux valeurs :</span><span class="sxs-lookup"><span data-stu-id="39c37-118">The STATFLAG enumeration has two values:</span></span><br/><span data-ttu-id="39c37-119">-STATFLAG_DEFAULT : 0</span><span class="sxs-lookup"><span data-stu-id="39c37-119">- STATFLAG_DEFAULT: 0</span></span><br/><span data-ttu-id="39c37-120">-STATFLAG_NONAME : 1</span><span class="sxs-lookup"><span data-stu-id="39c37-120">- STATFLAG_NONAME: 1</span></span> |


## <a name="remarks"></a><span data-ttu-id="39c37-121">Notes</span><span class="sxs-lookup"><span data-stu-id="39c37-121">Remarks</span></span>

<span data-ttu-id="39c37-122">La version de la méthode Stat implémentée pour l'objet Stream ADO remplit les champs de la structure STATSTG suivants :</span><span class="sxs-lookup"><span data-stu-id="39c37-122">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:</span></span>

|<span data-ttu-id="39c37-123">Champ</span><span class="sxs-lookup"><span data-stu-id="39c37-123">Field</span></span>|<span data-ttu-id="39c37-124">Description</span><span class="sxs-lookup"><span data-stu-id="39c37-124">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="39c37-125">*pwcsName*</span><span class="sxs-lookup"><span data-stu-id="39c37-125">*pwcsName*</span></span> |<span data-ttu-id="39c37-126">Une chaîne contenant le nom du flux, si elle est disponible et le StatFlag valeur STATFLAG\_anonyme n’a pas été spécifié.</span><span class="sxs-lookup"><span data-stu-id="39c37-126">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG\_NONAME was not specified.</span></span>|
|<span data-ttu-id="39c37-127">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="39c37-127">*cbSize*</span></span> |<span data-ttu-id="39c37-128">Indique la taille en octets du flux ou du tableau d'octets.</span><span class="sxs-lookup"><span data-stu-id="39c37-128">Specifies the size in bytes of the stream or byte array.</span></span>|
|<span data-ttu-id="39c37-129">*mtime*</span><span class="sxs-lookup"><span data-stu-id="39c37-129">*mtime*</span></span> |<span data-ttu-id="39c37-130">Indique l'heure de dernière modification de ce stockage, flux ou tableau d'octets.</span><span class="sxs-lookup"><span data-stu-id="39c37-130">Indicates the last modification time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="39c37-131">*ctime*</span><span class="sxs-lookup"><span data-stu-id="39c37-131">*ctime*</span></span> |<span data-ttu-id="39c37-132">Indique l'heure de création de ce stockage, flux ou tableau d'octets.</span><span class="sxs-lookup"><span data-stu-id="39c37-132">Indicates the creation time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="39c37-133">*atime*</span><span class="sxs-lookup"><span data-stu-id="39c37-133">*atime*</span></span> |<span data-ttu-id="39c37-134">Indique l'heure du dernier accès à ce stockage, flux ou tableau d'octets.</span><span class="sxs-lookup"><span data-stu-id="39c37-134">Indicates the last access time for this storage, stream or byte array.</span></span>|

<span data-ttu-id="39c37-135">Si STATFLAG\_anonyme est spécifié dans le paramètre StatFlag, le nom du flux n’est pas retourné.</span><span class="sxs-lookup"><span data-stu-id="39c37-135">If STATFLAG\_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</span></span>

<span data-ttu-id="39c37-136">Si STATFLAG\_anonyme n’a pas été spécifié dans le paramètre StatFlag et aucun nom n’est disponible pour le flux actif, cette valeur sera E\_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="39c37-136">If STATFLAG\_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E\_NOTIMPL.</span></span>

