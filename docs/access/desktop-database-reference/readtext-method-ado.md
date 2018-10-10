---
title: ReadText, méthode (ADO)
TOCTitle: ReadText Method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a44a3a002d390879e5d56d9c6931a91cba40271
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469108"
---
# <a name="readtext-method-ado"></a><span data-ttu-id="2bc6d-102">ReadText, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="2bc6d-102">ReadText Method (ADO)</span></span>


<span data-ttu-id="2bc6d-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2bc6d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2bc6d-104">Lit un nombre spécifié de caractères dans un objet [Stream](stream-object-ado.md) de texte.</span><span class="sxs-lookup"><span data-stu-id="2bc6d-104">Reads specified number of characters from a text [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bc6d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2bc6d-105">Syntax</span></span>

<span data-ttu-id="2bc6d-106">*Chaîne* = *flux*. ReadText (*NumChars*)</span><span class="sxs-lookup"><span data-stu-id="2bc6d-106">*String* = *Stream*.ReadText (*NumChars*)</span></span>

## <a name="parameters"></a><span data-ttu-id="2bc6d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2bc6d-107">Parameters</span></span>

  - <span data-ttu-id="2bc6d-108">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="2bc6d-108">*NumChars*</span></span>

  - <span data-ttu-id="2bc6d-p101">Facultatif. Valeur de type **Long** qui spécifie le nombre de caractères à lire dans le fichier ou une valeur [StreamReadEnum](streamreadenum.md). La valeur par défaut est **adReadAll**.</span><span class="sxs-lookup"><span data-stu-id="2bc6d-p101">Optional. A **Long** value that specifies the number of characters to read from the file, or a [StreamReadEnum](streamreadenum.md) value. The default value is **adReadAll**.</span></span>

## <a name="return-value"></a><span data-ttu-id="2bc6d-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2bc6d-112">Return Value</span></span>

<span data-ttu-id="2bc6d-113">La méthode **ReadText** lit un nombre spécifié de caractères, une ligne complète ou l'intégralité du flux d'un objet **Stream** et retourne la chaîne résultante.</span><span class="sxs-lookup"><span data-stu-id="2bc6d-113">The **ReadText** method reads a specified number of characters, an entire line, or the entire stream from a **Stream** object and returns the resulting string.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bc6d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="2bc6d-114">Remarks</span></span>

<span data-ttu-id="2bc6d-p102">Si la valeur de *NbCaractères* est supérieure au nombre de caractères encore présents dans le flux, seuls les caractères restants sont retournés. La chaîne lue n'est pas remplie pour correspondre à la longueur spécifiée par *NbCaractères*. S'il ne reste plus de caractères à lire, une valeur de type Variant NULL est retournée. La méthode **ReadText** ne peut pas être utilisée pour lire à l'envers.</span><span class="sxs-lookup"><span data-stu-id="2bc6d-p102">If *NumChar* is more than the number of characters left in the stream, only the characters remaining are returned. The string read is not padded to match the length specified by *NumChar*. If there are no characters left to read, a variant whose value is null is returned. **ReadText** cannot be used to read backwards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2bc6d-p103">La méthode <STRONG>ReadText</STRONG> est utilisée avec les flux de texte (<A href="type-property-ado-stream.md">Type </A><STRONG>adTypeText</STRONG>). Pour les flux binaires (<STRONG>Type </STRONG><STRONG>adTypeBinary</STRONG>), utilisez la méthode <A href="read-method-ado.md">Read</A>.</span><span class="sxs-lookup"><span data-stu-id="2bc6d-p103">The <STRONG>ReadText</STRONG> method is used with text streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>). For binary streams (<STRONG>Type</STRONG> is <STRONG>adTypeBinary</STRONG>), use <A href="read-method-ado.md">Read</A>.</span></span></P>


