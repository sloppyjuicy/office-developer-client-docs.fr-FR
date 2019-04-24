---
title: SendEmail, action de macro
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c0fa220b3088cde46b0e82631c06520afd839c64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314650"
---
# <a name="sendemail-macro-action"></a><span data-ttu-id="3d28d-102">SendEmail, action de macro</span><span class="sxs-lookup"><span data-stu-id="3d28d-102">SendEmail macro action</span></span>

<span data-ttu-id="3d28d-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d28d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3d28d-104">L'action **SendEmail** envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="3d28d-104">The **SendEmail** action sends an email message.</span></span>

> [!NOTE]
> <span data-ttu-id="3d28d-105">L’action **EnvoyerMessage** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="3d28d-105">The **SendEmail** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="3d28d-106">Setting</span><span class="sxs-lookup"><span data-stu-id="3d28d-106">Setting</span></span>

<span data-ttu-id="3d28d-107">L’action **EnvoyerMessage** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="3d28d-107">The **SendEmail** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d28d-108">Argument</span><span class="sxs-lookup"><span data-stu-id="3d28d-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="3d28d-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3d28d-109">Required</span></span></p></th>
<th><p><span data-ttu-id="3d28d-110">Description</span><span class="sxs-lookup"><span data-stu-id="3d28d-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d28d-111"><strong>To</strong></span><span class="sxs-lookup"><span data-stu-id="3d28d-111"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="3d28d-112">Oui</span><span class="sxs-lookup"><span data-stu-id="3d28d-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="3d28d-113">Destinataires du message dont les noms doivent être placés sur la ligne <strong>à</strong> du message. Séparez les noms des destinataires que vous spécifiez dans cet argument (et dans les arguments <em>CC</em> et <em>BCC</em> ) par un point-virgule (;).</span><span class="sxs-lookup"><span data-stu-id="3d28d-113">The recipients of the message whose names you want to put on the <strong>To</strong> line in the message.Separate the recipient names that you specify in this argument (and in the <em>Cc</em> and <em>Bcc</em> arguments) with a semicolon (;).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d28d-114"><strong>Cc</strong></span><span class="sxs-lookup"><span data-stu-id="3d28d-114"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="3d28d-115">Non</span><span class="sxs-lookup"><span data-stu-id="3d28d-115">No</span></span></p></td>
<td><p><span data-ttu-id="3d28d-116">Destinataires du message dont les noms doivent être placés sur la ligne&quot;CC (&quot;copie carbone) du message.</span><span class="sxs-lookup"><span data-stu-id="3d28d-116">The message recipients whose names you want to put on the Cc (&quot;carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d28d-117"><strong>Bcc</strong></span><span class="sxs-lookup"><span data-stu-id="3d28d-117"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="3d28d-118">Non</span><span class="sxs-lookup"><span data-stu-id="3d28d-118">No</span></span></p></td>
<td><p><span data-ttu-id="3d28d-119">Destinataires du message dont les noms doivent être placés sur la ligne&quot;CCI (copie&quot;carbone invisible) du message.</span><span class="sxs-lookup"><span data-stu-id="3d28d-119">The message recipients whose names you want to put on the Bcc (&quot;blind carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d28d-120"><strong>Subject</strong></span><span class="sxs-lookup"><span data-stu-id="3d28d-120"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="3d28d-121">Non</span><span class="sxs-lookup"><span data-stu-id="3d28d-121">No</span></span></p></td>
<td><p><span data-ttu-id="3d28d-p101">Objet du message. Ce texte apparaît sur la ligne <strong>Objet</strong> du message.</span><span class="sxs-lookup"><span data-stu-id="3d28d-p101">The subject of the message. This text appears on the <strong>Subject</strong> line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d28d-124"><strong>Body</strong></span><span class="sxs-lookup"><span data-stu-id="3d28d-124"><strong>Body</strong></span></span></p></td>
<td><p><span data-ttu-id="3d28d-125">Non</span><span class="sxs-lookup"><span data-stu-id="3d28d-125">No</span></span></p></td>
<td><p><span data-ttu-id="3d28d-p102">Texte que vous souhaitez inclure dans le corps du message électronique. Si vous laissez cet argument vide, aucun texte supplémentaire n’est inclus dans le message.</span><span class="sxs-lookup"><span data-stu-id="3d28d-p102">The text that you want to include in the main body of the mail message. If you leave this argument blank, no additional text is included in the message.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3d28d-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="3d28d-128">Remarks</span></span>

<span data-ttu-id="3d28d-129">L'action **EnvoyerMessage** est disponible uniquement dans les événements de macros **[Après suppression](after-delete-macro-event.md)**, **[Après insertion](after-insert-macro-event.md)** et **[Après MAJ](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="3d28d-129">The **SendEmail** action is available only in the **[After Delete](after-delete-macro-event.md)**, **[After Insert](after-insert-macro-event.md)**, and **[After Update](after-update-macro-event.md)** macro events.</span></span>

<span data-ttu-id="3d28d-130">L'action **EnvoyerMessage** n'affiche pas le message en vue de sa modification.</span><span class="sxs-lookup"><span data-stu-id="3d28d-130">The **SendEmail** action does not display the message for editing.</span></span>

