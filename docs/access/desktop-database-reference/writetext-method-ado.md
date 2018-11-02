---
title: WriteText, méthode (ADO)
TOCTitle: WriteText method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c0c4668141c0da6e5faddee009d2548f1ee2c53
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926996"
---
# <a name="writetext-method-ado"></a><span data-ttu-id="9129b-102">WriteText, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="9129b-102">WriteText method (ADO)</span></span>


<span data-ttu-id="9129b-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9129b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9129b-104">Écrit une chaîne de texte spécifiée dans un objet [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9129b-104">Writes a specified text string to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9129b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9129b-105">Syntax</span></span>

<span data-ttu-id="9129b-106">*Flux de données*. WriteText les*données*, *Options*</span><span class="sxs-lookup"><span data-stu-id="9129b-106">*Stream*.WriteText*Data*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="9129b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9129b-107">Parameters</span></span>

  - <span data-ttu-id="9129b-108">*Data*</span><span class="sxs-lookup"><span data-stu-id="9129b-108">*Data*</span></span>

  - <span data-ttu-id="9129b-109">Valeur de type **String** contenant les caractères du texte à écrire.</span><span class="sxs-lookup"><span data-stu-id="9129b-109">A **String** value that contains the text in characters to be written.</span></span>

  - <span data-ttu-id="9129b-110">*Options*</span><span class="sxs-lookup"><span data-stu-id="9129b-110">*Options*</span></span>

  - <span data-ttu-id="9129b-p101">Facultatif. Valeur [StreamWriteEnum](streamwriteenum.md) spécifiant si un séparateur de ligne doit être écrit à la fin de la chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9129b-p101">Optional. A [StreamWriteEnum](streamwriteenum.md) value that specifies whether a line separator character must be written at the end of the specified string.</span></span>

## <a name="remarks"></a><span data-ttu-id="9129b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9129b-113">Remarks</span></span>

<span data-ttu-id="9129b-114">Les chaînes spécifiées sont écrites dans l'objet **Stream** sans espace ou caractère inséré entre chaque chaîne.</span><span class="sxs-lookup"><span data-stu-id="9129b-114">Specified strings are written to the **Stream** object without any intervening spaces or characters between each string.</span></span>

<span data-ttu-id="9129b-p102">La propriété [Position](position-property-ado.md) actuelle est définie sur le caractère suivant les données écrites. La méthode **WriteText** ne tronque pas le reste des données d'un flux. Si vous souhaitez tronquer ces caractères, appelez [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9129b-p102">The current [Position](position-property-ado.md) is set to the character following the written data. The **WriteText** method does not truncate the rest of the data in a stream. If you want to truncate these characters, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="9129b-118">Si vous écrivez après la position [EOS](eos-property-ado.md) actuelle, la valeur de la propriété [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) de l'objet **Stream** augmente pour contenir les nouveaux caractères éventuels et **EOS** est déplacé au nouveau dernier octet de l'objet **Stream**.</span><span class="sxs-lookup"><span data-stu-id="9129b-118">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** will be increased to contain any new characters, and **EOS** will move to the new last byte in the **Stream**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="9129b-p103">La méthode <STRONG>WriteText</STRONG> est utilisée avec des flux de texte (<A href="type-property-ado-stream.md">Type</A> a la valeur <STRONG>adTypeText</STRONG>). Pour les flux binaires (<STRONG>Type</STRONG> a la valeur <STRONG>adTypeBinary</STRONG>), utilisez la méthode <A href="write-method-ado.md">Write</A>.</span><span class="sxs-lookup"><span data-stu-id="9129b-p103">The <STRONG>WriteText</STRONG> method is used with text streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>). For binary streams (<STRONG>Type</STRONG> is <STRONG>adTypeBinary</STRONG>), use <A href="write-method-ado.md">Write</A>.</span></span></P>


