---
title: ReadText, méthode (ADO)
TOCTitle: ReadText Method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5083dccd2c1d328e825a198008fd773bc3a592f6
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605211"
---
# <a name="readtext-method-ado"></a><span data-ttu-id="68de3-102">ReadText, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="68de3-102">ReadText Method (ADO)</span></span>


<span data-ttu-id="68de3-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="68de3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="68de3-104">Lit un nombre spécifié de caractères dans un objet [Stream](stream-object-ado.md) de texte.</span><span class="sxs-lookup"><span data-stu-id="68de3-104">Reads specified number of characters from a text [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="68de3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68de3-105">Syntax</span></span>

<span data-ttu-id="68de3-106">*Chaîne* = *flux*. ReadText (*NumChars*)</span><span class="sxs-lookup"><span data-stu-id="68de3-106">*String* = *Stream*.ReadText (*NumChars*)</span></span>

## <a name="parameters"></a><span data-ttu-id="68de3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68de3-107">Parameters</span></span>

  - <span data-ttu-id="68de3-108">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="68de3-108">*NumChars*</span></span>

  - <span data-ttu-id="68de3-p101">Facultatif. Valeur de type **Long** qui spécifie le nombre de caractères à lire dans le fichier ou une valeur [StreamReadEnum](streamreadenum.md). La valeur par défaut est **adReadAll**.</span><span class="sxs-lookup"><span data-stu-id="68de3-p101">Optional. A **Long** value that specifies the number of characters to read from the file, or a [StreamReadEnum](streamreadenum.md) value. The default value is **adReadAll**.</span></span>

<span data-ttu-id="68de3-112"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="68de3-112"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="68de3-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="68de3-113">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="68de3-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="68de3-114">Return value</span></span>
>>>>>>> <span data-ttu-id="68de3-115">master</span><span class="sxs-lookup"><span data-stu-id="68de3-115">master</span></span>

<span data-ttu-id="68de3-116">La méthode **ReadText** lit un nombre spécifié de caractères, une ligne complète ou l'intégralité du flux d'un objet **Stream** et retourne la chaîne résultante.</span><span class="sxs-lookup"><span data-stu-id="68de3-116">The **ReadText** method reads a specified number of characters, an entire line, or the entire stream from a **Stream** object and returns the resulting string.</span></span>

## <a name="remarks"></a><span data-ttu-id="68de3-117">Notes</span><span class="sxs-lookup"><span data-stu-id="68de3-117">Remarks</span></span>

<span data-ttu-id="68de3-p102">Si la valeur de *NbCaractères* est supérieure au nombre de caractères encore présents dans le flux, seuls les caractères restants sont retournés. La chaîne lue n'est pas remplie pour correspondre à la longueur spécifiée par *NbCaractères*. S'il ne reste plus de caractères à lire, une valeur de type Variant NULL est retournée. La méthode **ReadText** ne peut pas être utilisée pour lire à l'envers.</span><span class="sxs-lookup"><span data-stu-id="68de3-p102">If *NumChar* is more than the number of characters left in the stream, only the characters remaining are returned. The string read is not padded to match the length specified by *NumChar*. If there are no characters left to read, a variant whose value is null is returned. **ReadText** cannot be used to read backwards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="68de3-p103">La méthode <STRONG>ReadText</STRONG> est utilisée avec les flux de texte (<A href="type-property-ado-stream.md">Type </A><STRONG>adTypeText</STRONG>). Pour les flux binaires (<STRONG>Type </STRONG><STRONG>adTypeBinary</STRONG>), utilisez la méthode <A href="read-method-ado.md">Read</A>.</span><span class="sxs-lookup"><span data-stu-id="68de3-p103">The <STRONG>ReadText</STRONG> method is used with text streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>). For binary streams (<STRONG>Type</STRONG> is <STRONG>adTypeBinary</STRONG>), use <A href="read-method-ado.md">Read</A>.</span></span></P>


