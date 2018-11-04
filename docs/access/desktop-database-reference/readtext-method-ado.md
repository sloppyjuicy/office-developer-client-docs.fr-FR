---
title: ReadText, méthode (ADO)
TOCTitle: ReadText method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 66db24f95e3f6338174be3a70ca75dbb3332adeb
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949389"
---
# <a name="readtext-method-ado"></a><span data-ttu-id="7b3af-102">ReadText, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="7b3af-102">ReadText method (ADO)</span></span>

<span data-ttu-id="7b3af-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7b3af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7b3af-104">Lit un nombre spécifié de caractères dans un objet [Stream](stream-object-ado.md) de texte.</span><span class="sxs-lookup"><span data-stu-id="7b3af-104">Reads specified number of characters from a text [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b3af-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b3af-105">Syntax</span></span>

<span data-ttu-id="7b3af-106">*Chaîne* = *flux*. ReadText (*NumChars*)</span><span class="sxs-lookup"><span data-stu-id="7b3af-106">*String* = *Stream*.ReadText (*NumChars*)</span></span>

## <a name="parameters"></a><span data-ttu-id="7b3af-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b3af-107">Parameters</span></span>

|<span data-ttu-id="7b3af-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7b3af-108">Parameter</span></span>|<span data-ttu-id="7b3af-109">Description</span><span class="sxs-lookup"><span data-stu-id="7b3af-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="7b3af-110">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="7b3af-110">*NumChars*</span></span> |<span data-ttu-id="7b3af-p101">Facultatif. Valeur de type **Long** qui spécifie le nombre de caractères à lire dans le fichier ou une valeur [StreamReadEnum](streamreadenum.md). La valeur par défaut est **adReadAll**.</span><span class="sxs-lookup"><span data-stu-id="7b3af-p101">Optional. A **Long** value that specifies the number of characters to read from the file, or a [StreamReadEnum](streamreadenum.md) value. The default value is **adReadAll**.</span></span>|

## <a name="return-value"></a><span data-ttu-id="7b3af-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7b3af-114">Return value</span></span>

<span data-ttu-id="7b3af-115">La méthode **ReadText** lit un nombre spécifié de caractères, une ligne complète ou l'intégralité du flux d'un objet **Stream** et retourne la chaîne résultante.</span><span class="sxs-lookup"><span data-stu-id="7b3af-115">The **ReadText** method reads a specified number of characters, an entire line, or the entire stream from a **Stream** object and returns the resulting string.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b3af-116">Notes</span><span class="sxs-lookup"><span data-stu-id="7b3af-116">Remarks</span></span>

<span data-ttu-id="7b3af-p102">Si la valeur de *NbCaractères* est supérieure au nombre de caractères encore présents dans le flux, seuls les caractères restants sont retournés. La chaîne lue n'est pas remplie pour correspondre à la longueur spécifiée par *NbCaractères*. S'il ne reste plus de caractères à lire, une valeur de type Variant NULL est retournée. La méthode **ReadText** ne peut pas être utilisée pour lire à l'envers.</span><span class="sxs-lookup"><span data-stu-id="7b3af-p102">If *NumChar* is more than the number of characters left in the stream, only the characters remaining are returned. The string read is not padded to match the length specified by *NumChar*. If there are no characters left to read, a variant whose value is null is returned. **ReadText** cannot be used to read backwards.</span></span>

> [!NOTE]
> <span data-ttu-id="7b3af-p103">La méthode **ReadText** est utilisée avec les flux de texte ([Type ](type-property-ado-stream.md)**adTypeText**). Pour les flux binaires (**Type \*\*\*\*adTypeBinary**), utilisez la méthode [Read](read-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="7b3af-p103">The **ReadText** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**). For binary streams (**Type** is **adTypeBinary**), use [Read](read-method-ado.md).</span></span>

