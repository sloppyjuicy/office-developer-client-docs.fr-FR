---
title: SaveToFile, méthode (ADO)
TOCTitle: SaveToFile method (ADO)
ms:assetid: db0fd95e-8ef3-af87-5346-8f8713153ca7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250104(v=office.15)
ms:contentKeyID: 48548097
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f3b08c9df435c7ce995a40af7b8ad5466b79245d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308924"
---
# <a name="savetofile-method-ado"></a><span data-ttu-id="2190d-102">SaveToFile, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="2190d-102">SaveToFile method (ADO)</span></span>

<span data-ttu-id="2190d-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2190d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2190d-104">Enregistre le contenu binaire d’un objet [Stream](stream-object-ado.md) dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="2190d-104">Saves the binary contents of a [Stream](stream-object-ado.md) to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2190d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2190d-105">Syntax</span></span>

<span data-ttu-id="2190d-106">*Stream*. SaveToFile*filename*, *SaveOptions*</span><span class="sxs-lookup"><span data-stu-id="2190d-106">*Stream*.SaveToFile*FileName*, *SaveOptions*</span></span>

## <a name="parameters"></a><span data-ttu-id="2190d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2190d-107">Parameters</span></span>

|<span data-ttu-id="2190d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2190d-108">Parameter</span></span>|<span data-ttu-id="2190d-109">Description</span><span class="sxs-lookup"><span data-stu-id="2190d-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2190d-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="2190d-110">*FileName*</span></span> |<span data-ttu-id="2190d-p101">Valeur de type **String** qui contient le nom complet du fichier dans lequel le contenu de l'objet **Stream** sera enregistré. Vous pouvez enregistrer dans tout emplacement local valide ou tout emplacement auquel vous avez accès via une valeur UNC.</span><span class="sxs-lookup"><span data-stu-id="2190d-p101">A **String** value that contains the fully-qualified name of the file to which the contents of the **Stream** will be saved. You can save to any valid local location, or any location you have access to via a UNC value.</span></span>|
|<span data-ttu-id="2190d-113">*SaveOptions*</span><span class="sxs-lookup"><span data-stu-id="2190d-113">*SaveOptions*</span></span> |<span data-ttu-id="2190d-p102">Valeur [SaveOptionsEnum](saveoptionsenum.md) qui spécifie si un nouveau fichier doit être créé par la méthode **SaveToFile**, s'il n'existe pas encore. La valeur par défaut est **adSaveCreateNotExists**. Avec ces options, vous pouvez déterminer qu'une erreur doit être générée lorsque le fichier spécifié n'existe pas. Vous pouvez également préciser que la méthode **SaveToFile** remplace le contenu actuel d'un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="2190d-p102">A [SaveOptionsEnum](saveoptionsenum.md) value that specifies whether a new file should be created by **SaveToFile**, if it does not already exist. Default value is **adSaveCreateNotExists**. With these options you can specify that an error occurs if the specified file does not exist. You can also specify that **SaveToFile** overwrites the current contents of an existing file.</span></span>|

> [!NOTE]
> <span data-ttu-id="2190d-118">Si vous remplacez un fichier existant (lorsque la valeur **adSaveCreateOverwrite** est définie), la méthode **SaveToFile** tronque tous les octets du fichier existant d’origine qui suivent la nouvelle propriété [EOS](eos-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="2190d-118">If you overwrite an existing file (when **adSaveCreateOverwrite** is set), **SaveToFile** truncates any bytes from the original existing file that follow the new [EOS](eos-property-ado.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2190d-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="2190d-119">Remarks</span></span>

<span data-ttu-id="2190d-p103">La méthode **SaveToFile** peut être utilisée pour copier le contenu d'un objet **Stream** vers un fichier local. Le contenu ou les propriétés de l'objet **Stream** ne sont en aucune façon modifiés. L'objet **Stream** doit être ouvert avant d'appeler **SaveToFile**.</span><span class="sxs-lookup"><span data-stu-id="2190d-p103">**SaveToFile** may be used to copy the contents of a **Stream** object to a local file. There is no change in the contents or properties of the **Stream** object. The **Stream** object must be open before calling **SaveToFile**.</span></span>

<span data-ttu-id="2190d-p104">Cette méthode ne modifie pas l'association entre l'objet **Stream** et sa source sous-jacente. L'objet **Stream** reste associé à l'URL ou à l'objet **Record** d'origine qui représentait sa source lors de son ouverture.</span><span class="sxs-lookup"><span data-stu-id="2190d-p104">This method does not change the association of the **Stream** object to its underlying source. The **Stream** object will still be associated with the original URL or **Record** that was its source when opened.</span></span>

<span data-ttu-id="2190d-125">Après une opération **SaveToFile**, la position active ([Position](position-property-ado.md)) dans le flux est définie au début du flux (0).</span><span class="sxs-lookup"><span data-stu-id="2190d-125">After a **SaveToFile** operation, the current position ([Position](position-property-ado.md)) in the stream is set to the beginning of the stream (0).</span></span>

