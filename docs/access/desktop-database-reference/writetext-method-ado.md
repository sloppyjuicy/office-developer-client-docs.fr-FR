---
title: WriteText, méthode (ADO)
TOCTitle: WriteText method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6aecdbee544d3b30a6f6386c98d3083bb1167539
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949802"
---
# <a name="writetext-method-ado"></a><span data-ttu-id="25a99-102">WriteText, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="25a99-102">WriteText method (ADO)</span></span>

<span data-ttu-id="25a99-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="25a99-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="25a99-104">Écrit une chaîne de texte spécifiée dans un objet [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="25a99-104">Writes a specified text string to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="25a99-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25a99-105">Syntax</span></span>

<span data-ttu-id="25a99-106">*Flux de données*. WriteText les*données*, *Options*</span><span class="sxs-lookup"><span data-stu-id="25a99-106">*Stream*.WriteText*Data*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="25a99-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25a99-107">Parameters</span></span>

|<span data-ttu-id="25a99-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="25a99-108">Parameter</span></span>|<span data-ttu-id="25a99-109">Description</span><span class="sxs-lookup"><span data-stu-id="25a99-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="25a99-110">*Data*</span><span class="sxs-lookup"><span data-stu-id="25a99-110">*Data*</span></span> |<span data-ttu-id="25a99-111">Valeur de type **String** contenant les caractères du texte à écrire.</span><span class="sxs-lookup"><span data-stu-id="25a99-111">A **String** value that contains the text in characters to be written.</span></span>|
|<span data-ttu-id="25a99-112">*Options*</span><span class="sxs-lookup"><span data-stu-id="25a99-112">*Options*</span></span> |<span data-ttu-id="25a99-p101">Facultatif. Valeur [StreamWriteEnum](streamwriteenum.md) spécifiant si un séparateur de ligne doit être écrit à la fin de la chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="25a99-p101">Optional. A [StreamWriteEnum](streamwriteenum.md) value that specifies whether a line separator character must be written at the end of the specified string.</span></span>|

## <a name="remarks"></a><span data-ttu-id="25a99-115">Notes</span><span class="sxs-lookup"><span data-stu-id="25a99-115">Remarks</span></span>

<span data-ttu-id="25a99-116">Les chaînes spécifiées sont écrites dans l'objet **Stream** sans espace ou caractère inséré entre chaque chaîne.</span><span class="sxs-lookup"><span data-stu-id="25a99-116">Specified strings are written to the **Stream** object without any intervening spaces or characters between each string.</span></span>

<span data-ttu-id="25a99-p102">La propriété [Position](position-property-ado.md) actuelle est définie sur le caractère suivant les données écrites. La méthode **WriteText** ne tronque pas le reste des données d'un flux. Si vous souhaitez tronquer ces caractères, appelez [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="25a99-p102">The current [Position](position-property-ado.md) is set to the character following the written data. The **WriteText** method does not truncate the rest of the data in a stream. If you want to truncate these characters, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="25a99-120">Si vous écrivez après la position [EOS](eos-property-ado.md) actuelle, la valeur de la propriété [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) de l'objet **Stream** augmente pour contenir les nouveaux caractères éventuels et **EOS** est déplacé au nouveau dernier octet de l'objet **Stream**.</span><span class="sxs-lookup"><span data-stu-id="25a99-120">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** will be increased to contain any new characters, and **EOS** will move to the new last byte in the **Stream**.</span></span>

> [!NOTE]
> <span data-ttu-id="25a99-p103">La méthode **WriteText** est utilisée avec des flux de texte ([Type](type-property-ado-stream.md) a la valeur **adTypeText**). Pour les flux binaires (**Type** a la valeur **adTypeBinary**), utilisez la méthode [Write](write-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="25a99-p103">The **WriteText** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**). For binary streams (**Type** is **adTypeBinary**), use [Write](write-method-ado.md).</span></span>


