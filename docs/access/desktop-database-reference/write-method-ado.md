---
title: Écrire, méthode - ActiveX Data Objects (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c6f4bba55ec3a32d206d3a7bfd001e96cd94923e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702515"
---
# <a name="write-method-ado"></a><span data-ttu-id="a890c-102">Write, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="a890c-102">Write method (ADO)</span></span>

<span data-ttu-id="a890c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a890c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a890c-104">Écrit des données binaires dans un objet [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a890c-104">Writes binary data to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a890c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a890c-105">Syntax</span></span>

<span data-ttu-id="a890c-106">*Flux de données*. Écrire la*mémoire tampon*</span><span class="sxs-lookup"><span data-stu-id="a890c-106">*Stream*.Write*Buffer*</span></span>

## <a name="parameters"></a><span data-ttu-id="a890c-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="a890c-107">Parameters</span></span>

|<span data-ttu-id="a890c-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a890c-108">Parameter</span></span>|<span data-ttu-id="a890c-109">Description</span><span class="sxs-lookup"><span data-stu-id="a890c-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a890c-110">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="a890c-110">*Buffer*</span></span> |<span data-ttu-id="a890c-111">Valeur de type **Variant** contenant un tableau d'octets à écrire.</span><span class="sxs-lookup"><span data-stu-id="a890c-111">A **Variant** that contains an array of bytes to be written.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a890c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a890c-112">Remarks</span></span>

<span data-ttu-id="a890c-113">Les octets spécifiés sont écrits dans l'objet **Stream** sans espaces insérés entre chaque octet.</span><span class="sxs-lookup"><span data-stu-id="a890c-113">Specified bytes are written to the **Stream** object without any intervening spaces between each byte.</span></span>

<span data-ttu-id="a890c-p101">La propriété [Position](position-property-ado.md) actuelle est définie par l'octet suivant les données écrites. La méthode **Write** ne tronque pas le reste des données d'un flux. Si vous souhaitez tronquer ces octets, appelez la méthode [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a890c-p101">The current [Position](position-property-ado.md) is set to the byte following the written data. The **Write** method does not truncate the rest of the data in a stream. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="a890c-117">Si vous écrivez après la position [EOS](eos-property-ado.md) actuelle, la valeur de la propriété [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) de l'objet **Stream** augmente pour contenir les nouveaux octets éventuels et **EOS** est déplacé au nouveau dernier octet de l'objet **Stream**.</span><span class="sxs-lookup"><span data-stu-id="a890c-117">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) of the **Stream** will be increased to contain any new bytes, and **EOS** will move to the new last byte in the **Stream**.</span></span>

> [!NOTE]
> <span data-ttu-id="a890c-p102">La méthode **Write** est utilisée avec des flux binaires ([Type](type-property-ado-stream.md) a la valeur **adTypeBinary**). Pour les flux de texte (**Type** a la valeur **adTypeText**), utilisez la méthode [WriteText](writetext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a890c-p102">The **Write** method is used with binary streams ([Type](type-property-ado-stream.md) is **adTypeBinary**). For text streams (**Type** is **adTypeText**), use [WriteText](writetext-method-ado.md).</span></span>

