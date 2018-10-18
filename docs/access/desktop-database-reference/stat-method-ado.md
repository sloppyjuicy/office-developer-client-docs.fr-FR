---
title: Méthode Stat - ActiveX Data Objects (ADO)
TOCTitle: Stat Method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6bc4ff8076ec07d065ba932ef0e0017edb97e703
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606954"
---
# <a name="stat-method-ado"></a><span data-ttu-id="d2150-102">Stat, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="d2150-102">Stat Method (ADO)</span></span>


<span data-ttu-id="d2150-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2150-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d2150-104">Extrait des informations relatives à un objet **Stream**.</span><span class="sxs-lookup"><span data-stu-id="d2150-104">Retrieves information about a **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2150-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2150-105">Syntax</span></span>

<span data-ttu-id="d2150-106">Longueur du *flux*. Stat (*StatStg*, *StatFlag*)</span><span class="sxs-lookup"><span data-stu-id="d2150-106">Long *stream*.Stat(*StatStg*, *StatFlag*)</span></span>

<span data-ttu-id="d2150-107"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="d2150-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="d2150-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d2150-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="d2150-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d2150-109">Return value</span></span>
>>>>>>> <span data-ttu-id="d2150-110">master</span><span class="sxs-lookup"><span data-stu-id="d2150-110">master</span></span>

<span data-ttu-id="d2150-111">Valeur de type Long indiquant l'état de l'opération.</span><span class="sxs-lookup"><span data-stu-id="d2150-111">A long value indicating the status of the operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2150-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2150-112">Parameters</span></span>

  - <span data-ttu-id="d2150-113">*StatStg*</span><span class="sxs-lookup"><span data-stu-id="d2150-113">*StatStg*</span></span>

  - <span data-ttu-id="d2150-p101">Structure STATSTG contenant des informations relatives au flux. L'implémentation de la méthode Stat utilisée par l'objet Stream ADO ne remplit pas tous les champs de la structure.</span><span class="sxs-lookup"><span data-stu-id="d2150-p101">A STATSTG structure that will be filled in with information about the stream. The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.</span></span>

  - <span data-ttu-id="d2150-116">*StatFlag*</span><span class="sxs-lookup"><span data-stu-id="d2150-116">*StatFlag*</span></span>

  - <span data-ttu-id="d2150-p102">Indique que cette méthode ne renvoie pas certains membres dans la structure STATSTG, ce qui permet d'éviter une opération d'allocation de mémoire. Les valeurs sont extraites de l'énumération STATFLAG.</span><span class="sxs-lookup"><span data-stu-id="d2150-p102">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation. Values are taken from the STATFLAG enumeration.</span></span>  
      
    <span data-ttu-id="d2150-119">L'énumération STATFLAG possède deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="d2150-119">The STATFLAG enumeration has two values</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="d2150-120">Constant</span><span class="sxs-lookup"><span data-stu-id="d2150-120">Constant</span></span></p></th>
    <th><p><span data-ttu-id="d2150-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2150-121">Value</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="d2150-122">STATFLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d2150-122">STATFLAG_DEFAULT</span></span></p></td>
    <td><p><span data-ttu-id="d2150-123">0</span><span class="sxs-lookup"><span data-stu-id="d2150-123">0</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="d2150-124">STATFLAG_NONAME</span><span class="sxs-lookup"><span data-stu-id="d2150-124">STATFLAG_NONAME</span></span></p></td>
    <td><p><span data-ttu-id="d2150-125">1</span><span class="sxs-lookup"><span data-stu-id="d2150-125">1</span></span></p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a><span data-ttu-id="d2150-126">Notes</span><span class="sxs-lookup"><span data-stu-id="d2150-126">Remarks</span></span>

<span data-ttu-id="d2150-127">La version de la méthode Stat implémentée pour l'objet Stream ADO remplit les champs de la structure STATSTG suivants :</span><span class="sxs-lookup"><span data-stu-id="d2150-127">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:</span></span>

  - <span data-ttu-id="d2150-128">*pwcsName*</span><span class="sxs-lookup"><span data-stu-id="d2150-128">*pwcsName*</span></span>

  - <span data-ttu-id="d2150-129">Une chaîne contenant le nom du flux, si elle est disponible et le StatFlag valeur STATFLAG\_anonyme n’a pas été spécifié.</span><span class="sxs-lookup"><span data-stu-id="d2150-129">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG\_NONAME was not specified.</span></span>

  - <span data-ttu-id="d2150-130">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="d2150-130">*cbSize*</span></span>

  - <span data-ttu-id="d2150-131">Indique la taille en octets du flux ou du tableau d'octets.</span><span class="sxs-lookup"><span data-stu-id="d2150-131">Specifies the size in bytes of the stream or byte array.</span></span>

  - <span data-ttu-id="d2150-132">*mtime*</span><span class="sxs-lookup"><span data-stu-id="d2150-132">*mtime*</span></span>

  - <span data-ttu-id="d2150-133">Indique l'heure de dernière modification de ce stockage, flux ou tableau d'octets.</span><span class="sxs-lookup"><span data-stu-id="d2150-133">Indicates the last modification time for this storage, stream, or byte array.</span></span>

  - <span data-ttu-id="d2150-134">*ctime*</span><span class="sxs-lookup"><span data-stu-id="d2150-134">*ctime*</span></span>

  - <span data-ttu-id="d2150-135">Indique l'heure de création de ce stockage, flux ou tableau d'octets.</span><span class="sxs-lookup"><span data-stu-id="d2150-135">Indicates the creation time for this storage, stream, or byte array.</span></span>

  - <span data-ttu-id="d2150-136">*atime*</span><span class="sxs-lookup"><span data-stu-id="d2150-136">*atime*</span></span>

  - <span data-ttu-id="d2150-137">Indique l'heure du dernier accès à ce stockage, flux ou tableau d'octets.</span><span class="sxs-lookup"><span data-stu-id="d2150-137">Indicates the last access time for this storage, stream or byte array.</span></span>

<span data-ttu-id="d2150-138">Si STATFLAG\_anonyme est spécifié dans le paramètre StatFlag, le nom du flux n’est pas retourné.</span><span class="sxs-lookup"><span data-stu-id="d2150-138">If STATFLAG\_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</span></span>

<span data-ttu-id="d2150-139">Si STATFLAG\_anonyme n’a pas été spécifié dans le paramètre StatFlag et aucun nom n’est disponible pour le flux actif, cette valeur sera E\_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="d2150-139">If STATFLAG\_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E\_NOTIMPL.</span></span>

