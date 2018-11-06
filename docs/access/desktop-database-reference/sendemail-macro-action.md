---
title: SendEmail, action de macro
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a5016500b62a465f21ecab93a6fb66c9e6d514e1
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998839"
---
# <a name="sendemail-macro-action"></a><span data-ttu-id="3363e-102">SendEmail, action de macro</span><span class="sxs-lookup"><span data-stu-id="3363e-102">SendEmail macro action</span></span>

<span data-ttu-id="3363e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3363e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3363e-104">L’action **EnvoyerMessage** envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="3363e-104">The **SendEmail** action sends an email message.</span></span>

> [!NOTE]
> <span data-ttu-id="3363e-105">[!REMARQUE] L'action **EnvoyerMessage** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="3363e-105">The **SendEmail** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="3363e-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3363e-106">Setting</span></span>

<span data-ttu-id="3363e-107">L'action **EnvoyerMessage** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="3363e-107">The **SendEmail** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3363e-108">Argument</span><span class="sxs-lookup"><span data-stu-id="3363e-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="3363e-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3363e-109">Required</span></span></p></th>
<th><p><span data-ttu-id="3363e-110">Description</span><span class="sxs-lookup"><span data-stu-id="3363e-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3363e-111"><strong>Pour</strong></span><span class="sxs-lookup"><span data-stu-id="3363e-111"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="3363e-112">Oui</span><span class="sxs-lookup"><span data-stu-id="3363e-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="3363e-113">Les destinataires du message dont les noms doivent figurer sur la ligne <strong>à</strong> du message. Séparez les noms des destinataires que vous spécifiez dans cet argument (et dans les arguments <em>Cc</em> et <em>Cci</em> ) par un point-virgule ( ;).</span><span class="sxs-lookup"><span data-stu-id="3363e-113">The recipients of the message whose names you want to put on the <strong>To</strong> line in the message.Separate the recipient names that you specify in this argument (and in the <em>Cc</em> and <em>Bcc</em> arguments) with a semicolon (;).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3363e-114"><strong>Cc</strong></span><span class="sxs-lookup"><span data-stu-id="3363e-114"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="3363e-115">Non</span><span class="sxs-lookup"><span data-stu-id="3363e-115">No</span></span></p></td>
<td><p><span data-ttu-id="3363e-116">Destinataires du message dont les noms doivent figurer sur la liste Cc (&quot;copie carbone&quot;) ligne du message.</span><span class="sxs-lookup"><span data-stu-id="3363e-116">The message recipients whose names you want to put on the Cc (&quot;carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3363e-117"><strong>Cci</strong></span><span class="sxs-lookup"><span data-stu-id="3363e-117"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="3363e-118">Non</span><span class="sxs-lookup"><span data-stu-id="3363e-118">No</span></span></p></td>
<td><p><span data-ttu-id="3363e-119">Destinataires du message dont les noms doivent figurer dans le champ Cci (&quot;copie carbone invisible&quot;) ligne du message.</span><span class="sxs-lookup"><span data-stu-id="3363e-119">The message recipients whose names you want to put on the Bcc (&quot;blind carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3363e-120"><strong>Objet</strong></span><span class="sxs-lookup"><span data-stu-id="3363e-120"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="3363e-121">Non</span><span class="sxs-lookup"><span data-stu-id="3363e-121">No</span></span></p></td>
<td><p><span data-ttu-id="3363e-p101">Objet du message. Ce texte apparaît sur la ligne <strong>Objet</strong> du message.</span><span class="sxs-lookup"><span data-stu-id="3363e-p101">The subject of the message. This text appears on the <strong>Subject</strong> line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3363e-124"><strong>Body</strong></span><span class="sxs-lookup"><span data-stu-id="3363e-124"><strong>Body</strong></span></span></p></td>
<td><p><span data-ttu-id="3363e-125">Non</span><span class="sxs-lookup"><span data-stu-id="3363e-125">No</span></span></p></td>
<td><p><span data-ttu-id="3363e-p102">Texte que vous souhaitez inclure dans le corps du message électronique. Si vous laissez cet argument vide, aucun texte supplémentaire n’est inclus dans le message.</span><span class="sxs-lookup"><span data-stu-id="3363e-p102">The text that you want to include in the main body of the mail message. If you leave this argument blank, no additional text is included in the message.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3363e-128">Notes</span><span class="sxs-lookup"><span data-stu-id="3363e-128">Remarks</span></span>

<span data-ttu-id="3363e-129">L'action **EnvoyerMessage** est disponible uniquement dans les événements de macros **[Après suppression](after-delete-macro-event.md)**, **[Après insertion](after-insert-macro-event.md)** et **[Après MAJ](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="3363e-129">The **SendEmail** action is available only in the **[After Delete](after-delete-macro-event.md)**, **[After Insert](after-insert-macro-event.md)**, and **[After Update](after-update-macro-event.md)** macro events.</span></span>

<span data-ttu-id="3363e-130">L'action **EnvoyerMessage** n'affiche pas le message en vue de sa modification.</span><span class="sxs-lookup"><span data-stu-id="3363e-130">The **SendEmail** action does not display the message for editing.</span></span>

