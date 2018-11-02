---
title: Écrire, méthode - ActiveX Data Objects (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a04825a59f19b6b54fbb10652a1bba2fd0479588
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920962"
---
# <a name="write-method-ado"></a><span data-ttu-id="59f26-102">Write, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="59f26-102">Write method (ADO)</span></span>


<span data-ttu-id="59f26-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="59f26-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="59f26-104">Écrit des données binaires dans un objet [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="59f26-104">Writes binary data to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="59f26-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59f26-105">Syntax</span></span>

<span data-ttu-id="59f26-106">*Flux de données*. Écrire la*mémoire tampon*</span><span class="sxs-lookup"><span data-stu-id="59f26-106">*Stream*.Write*Buffer*</span></span>

## <a name="parameters"></a><span data-ttu-id="59f26-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59f26-107">Parameters</span></span>

  - <span data-ttu-id="59f26-108">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="59f26-108">*Buffer*</span></span>

  - <span data-ttu-id="59f26-109">Valeur de type **Variant** contenant un tableau d'octets à écrire.</span><span class="sxs-lookup"><span data-stu-id="59f26-109">A **Variant** that contains an array of bytes to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="59f26-110">Notes</span><span class="sxs-lookup"><span data-stu-id="59f26-110">Remarks</span></span>

<span data-ttu-id="59f26-111">Les octets spécifiés sont écrits dans l'objet **Stream** sans espaces insérés entre chaque octet.</span><span class="sxs-lookup"><span data-stu-id="59f26-111">Specified bytes are written to the **Stream** object without any intervening spaces between each byte.</span></span>

<span data-ttu-id="59f26-p101">La propriété [Position](position-property-ado.md) actuelle est définie par l'octet suivant les données écrites. La méthode **Write** ne tronque pas le reste des données d'un flux. Si vous souhaitez tronquer ces octets, appelez la méthode [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="59f26-p101">The current [Position](position-property-ado.md) is set to the byte following the written data. The **Write** method does not truncate the rest of the data in a stream. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="59f26-115">Si vous écrivez après la position [EOS](eos-property-ado.md) actuelle, la valeur de la propriété [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) de l'objet **Stream** augmente pour contenir les nouveaux octets éventuels et **EOS** est déplacé au nouveau dernier octet de l'objet **Stream**.</span><span class="sxs-lookup"><span data-stu-id="59f26-115">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** will be increased to contain any new bytes, and **EOS** will move to the new last byte in the **Stream**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="59f26-p102">La méthode <STRONG>Write</STRONG> est utilisée avec des flux binaires (<A href="type-property-ado-stream.md">Type</A> a la valeur <STRONG>adTypeBinary</STRONG>). Pour les flux de texte (<STRONG>Type</STRONG> a la valeur <STRONG>adTypeText</STRONG>), utilisez la méthode <A href="writetext-method-ado.md">WriteText</A>.</span><span class="sxs-lookup"><span data-stu-id="59f26-p102">The <STRONG>Write</STRONG> method is used with binary streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeBinary</STRONG>). For text streams (<STRONG>Type</STRONG> is <STRONG>adTypeText</STRONG>), use <A href="writetext-method-ado.md">WriteText</A>.</span></span></P>


