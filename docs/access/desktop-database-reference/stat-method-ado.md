---
title: Stat, méthode - ActiveX Data Objects (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 853d89bde9184bd546b3e7df9e8eda287faf86c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308548"
---
# <a name="stat-method-ado"></a><span data-ttu-id="daf05-102">Stat, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="daf05-102">Stat method (ADO)</span></span>

<span data-ttu-id="daf05-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="daf05-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="daf05-104">Extrait des informations relatives à un objet **Stream**.</span><span class="sxs-lookup"><span data-stu-id="daf05-104">Retrieves information about a **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="daf05-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="daf05-105">Syntax</span></span>

<span data-ttu-id="daf05-106">Flux *long*. Stat(*StatStg*, *StatFlag*)</span><span class="sxs-lookup"><span data-stu-id="daf05-106">Long *stream*.Stat(*StatStg*, *StatFlag*)</span></span>

## <a name="return-value"></a><span data-ttu-id="daf05-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="daf05-107">Return value</span></span>

<span data-ttu-id="daf05-108">Valeur de type Long indiquant l'état de l'opération.</span><span class="sxs-lookup"><span data-stu-id="daf05-108">A long value indicating the status of the operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="daf05-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="daf05-109">Parameters</span></span>

|<span data-ttu-id="daf05-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="daf05-110">Parameter</span></span>|<span data-ttu-id="daf05-111">Description</span><span class="sxs-lookup"><span data-stu-id="daf05-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="daf05-112">*StatStg*</span><span class="sxs-lookup"><span data-stu-id="daf05-112">*StatStg*</span></span> |<span data-ttu-id="daf05-p101">Structure STATSTG contenant des informations relatives au flux. L'implémentation de la méthode Stat utilisée par l'objet Stream ADO ne remplit pas tous les champs de la structure.</span><span class="sxs-lookup"><span data-stu-id="daf05-p101">A STATSTG structure that will be filled in with information about the stream. The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.</span></span>|
|<span data-ttu-id="daf05-115">*StatFlag*</span><span class="sxs-lookup"><span data-stu-id="daf05-115">*StatFlag*</span></span> |<span data-ttu-id="daf05-p102">Indique que cette méthode ne renvoie pas certains membres dans la structure STATSTG, ce qui permet d'éviter une opération d'allocation de mémoire. Les valeurs sont extraites de l'énumération STATFLAG.</span><span class="sxs-lookup"><span data-stu-id="daf05-p102">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation. Values are taken from the STATFLAG enumeration.</span></span><br/><br/><span data-ttu-id="daf05-118">L’éumération STATFLAG a deux valeurs :</span><span class="sxs-lookup"><span data-stu-id="daf05-118">The STATFLAG enumeration has two values:</span></span><br/><span data-ttu-id="daf05-119">- STATFLAG_DEFAULT : 0</span><span class="sxs-lookup"><span data-stu-id="daf05-119">- STATFLAG_DEFAULT: 0</span></span><br/><span data-ttu-id="daf05-120">- STATFLAG_NONAME : 1</span><span class="sxs-lookup"><span data-stu-id="daf05-120">- STATFLAG_NONAME: 1</span></span> |


## <a name="remarks"></a><span data-ttu-id="daf05-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="daf05-121">Remarks</span></span>

<span data-ttu-id="daf05-122">La version de la méthode Stat implémentée pour l'objet Stream ADO remplit les champs de la structure STATSTG suivants :</span><span class="sxs-lookup"><span data-stu-id="daf05-122">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:</span></span>

|<span data-ttu-id="daf05-123">Champ</span><span class="sxs-lookup"><span data-stu-id="daf05-123">Field</span></span>|<span data-ttu-id="daf05-124">Description</span><span class="sxs-lookup"><span data-stu-id="daf05-124">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="daf05-125">*pwcsName*</span><span class="sxs-lookup"><span data-stu-id="daf05-125">*pwcsName*</span></span> |<span data-ttu-id="daf05-126">Chaîne contenant le nom du flux, si une chaîne est disponible et si la valeur STATFlag \_ STATFLAG NONAME n’a pas été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="daf05-126">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG\_NONAME was not specified.</span></span>|
|<span data-ttu-id="daf05-127">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="daf05-127">*cbSize*</span></span> |<span data-ttu-id="daf05-128">Indique la taille en octets du flux ou du tableau d'octets.</span><span class="sxs-lookup"><span data-stu-id="daf05-128">Specifies the size in bytes of the stream or byte array.</span></span>|
|<span data-ttu-id="daf05-129">*mtime*</span><span class="sxs-lookup"><span data-stu-id="daf05-129">*mtime*</span></span> |<span data-ttu-id="daf05-130">Indique l'heure de dernière modification de ce stockage, flux ou tableau d'octets.</span><span class="sxs-lookup"><span data-stu-id="daf05-130">Indicates the last modification time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="daf05-131">*ctime*</span><span class="sxs-lookup"><span data-stu-id="daf05-131">*ctime*</span></span> |<span data-ttu-id="daf05-132">Indique l'heure de création de ce stockage, flux ou tableau d'octets.</span><span class="sxs-lookup"><span data-stu-id="daf05-132">Indicates the creation time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="daf05-133">*atime*</span><span class="sxs-lookup"><span data-stu-id="daf05-133">*atime*</span></span> |<span data-ttu-id="daf05-134">Indique l'heure du dernier accès à ce stockage, flux ou tableau d'octets.</span><span class="sxs-lookup"><span data-stu-id="daf05-134">Indicates the last access time for this storage, stream or byte array.</span></span>|

<span data-ttu-id="daf05-135">Si STATFLAG NONAME est spécifié dans le paramètre StatFlag, le nom du flux \_ n’est pas renvoyé.</span><span class="sxs-lookup"><span data-stu-id="daf05-135">If STATFLAG\_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</span></span>

<span data-ttu-id="daf05-136">Si STATFLAG NONAME n’a pas été spécifié dans le paramètre StatFlag et qu’aucun nom n’est disponible pour le flux actuel, cette valeur sera \_ E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="daf05-136">If STATFLAG\_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E\_NOTIMPL.</span></span>

