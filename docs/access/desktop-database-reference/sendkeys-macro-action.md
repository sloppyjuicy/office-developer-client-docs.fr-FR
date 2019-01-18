---
title: SendKeys, action de macro
TOCTitle: SendKeys macro action
ms:assetid: 3b06fcfc-ea64-c780-b5fc-6fc72853f524
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192656(v=office.15)
ms:contentKeyID: 48544275
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm183441
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f8c45cdf0d9cf588f61d1b51b728a8a15f6d7e12
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722374"
---
# <a name="sendkeys-macro-action"></a><span data-ttu-id="10abc-102">SendKeys, action de macro</span><span class="sxs-lookup"><span data-stu-id="10abc-102">SendKeys macro action</span></span>

<span data-ttu-id="10abc-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="10abc-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Remarque sur la sécurité" alt="Security note" /><span data-ttu-id="10abc-105">de sécurité\*\*</span><span class="sxs-lookup"><span data-stu-id="10abc-105"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10abc-p101">
      Évitez d’utiliser l’instruction <strong>SendKeys</strong> ou une macro AutoKeys avec des informations sensibles et confidentielles. Un utilisateur malveillant pourrait intercepter la frappe et compromettre la sécurité de votre ordinateur et de vos données.
</span><span class="sxs-lookup"><span data-stu-id="10abc-p101">Avoid using the <strong>SendKeys</strong> statement or an AutoKeys macro with sensitive or confidential information. A malicious user could intercept the keystrokes and compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10abc-108">Vous pouvez utiliser l'action **EnvoiTouches** pour envoyer directement une séquence de touches à Microsoft Access ou à une application Windows active.</span><span class="sxs-lookup"><span data-stu-id="10abc-108">You can use the **SendKeys** action to send keystrokes directly to Microsoft Access or to an active Windows-based application.</span></span>

> [!NOTE]
> <span data-ttu-id="10abc-109">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="10abc-109">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="10abc-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="10abc-110">Setting</span></span>

<span data-ttu-id="10abc-111">L'action **EnvoiTouches** accepte les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="10abc-111">The **SendKeys** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10abc-112">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="10abc-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="10abc-113">Description</span><span class="sxs-lookup"><span data-stu-id="10abc-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10abc-114"><strong>Touches</strong></span><span class="sxs-lookup"><span data-stu-id="10abc-114"><strong>Keystrokes</strong></span></span></p></td>
<td><p><span data-ttu-id="10abc-p102">Séquence de touches qu’Access ou l’application doit traiter. Entrez la séquence de touches dans la zone <strong>Touches</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Cette zone peut contenir jusqu’à 255 caractères. Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="10abc-p102">The keystrokes you want Access or the application to process. Enter the keystrokes in the <strong>Keystrokes</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can type up to 255 characters. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10abc-119"><strong>Wait</strong></span><span class="sxs-lookup"><span data-stu-id="10abc-119"><strong>Wait</strong></span></span></p></td>
<td><p><span data-ttu-id="10abc-p103">Spécifie si la macro doit attendre que la séquence de touches ait été traitée. Cliquez sur <strong>Oui</strong> (pour attendre) ou <strong>Non</strong> (pour ne pas attendre). La valeur par défaut est <strong>Non</strong>.</span><span class="sxs-lookup"><span data-stu-id="10abc-p103">Specifies whether the macro should pause until the keystrokes have been processed. Click <strong>Yes</strong> (to pause) or <strong>No</strong> (to not pause). The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="10abc-123">Notes</span><span class="sxs-lookup"><span data-stu-id="10abc-123">Remarks</span></span>

<span data-ttu-id="10abc-124">Access traite la séquence de touches qu'il reçoit via l'action **EnvoiTouches** comme si vous l'aviez tapée directement dans une fenêtre Access.</span><span class="sxs-lookup"><span data-stu-id="10abc-124">Access processes the keystrokes it receives through the **SendKeys** action exactly as if you had typed them directly in an Access window.</span></span>

<span data-ttu-id="10abc-125">Pour spécifier la séquence de touches, utilisez la même syntaxe que celle utilisée dans l'instruction **EnvoiTouches**.</span><span class="sxs-lookup"><span data-stu-id="10abc-125">To specify the keystrokes, use the same syntax as you would for the **SendKeys** statement.</span></span>

> [!NOTE]
> <span data-ttu-id="10abc-126">[!REMARQUE] Une erreur peut se produire si l'argument **Touches** contient une syntaxe incorrecte, du texte mal orthographié ou des valeurs non appropriées pour la fenêtre à laquelle la séquence de touches est envoyée.</span><span class="sxs-lookup"><span data-stu-id="10abc-126">An error can occur if the **Keystrokes** argument contains incorrect syntax, misspelled text, or other values that aren't appropriate for the window the keystrokes are sent to.</span></span>

<span data-ttu-id="10abc-p104">Vous pouvez utiliser cette action pour entrer des informations dans une boîte de dialogue, notamment si vous ne voulez pas interrompre la macro pour répondre manuellement à la boîte de dialogue. Certaines actions Access, telles que **Imprimer** et **TrouverEnregistrement**, sélectionnent automatiquement les options de certaines boîtes de dialogue souvent utilisées. Vous pouvez utiliser l'action **EnvoiTouches** pour sélectionner des options de boîte de dialogue moins utilisées.</span><span class="sxs-lookup"><span data-stu-id="10abc-p104">You can use this action to enter information in a dialog box, particularly if you don't want to interrupt the macro to respond manually to the dialog box. Some Access actions, such as **PrintOut** and **FindRecord**, automatically select the options in certain frequently used dialog boxes. You can use the **SendKeys** action to select the options in less commonly used dialog boxes.</span></span>

> [!NOTE]
> - <span data-ttu-id="10abc-130">Dans la mesure où la boîte de dialogue interrompt la macro, vous devez placer l'action **EnvoiTouches** avant l'action qui entraîne l'ouverture de la boîte de dialogue et définir l'argument **Attendre** la valeur sur **Non**.</span><span class="sxs-lookup"><span data-stu-id="10abc-130">Because the dialog box suspends the macro, you must put the **SendKeys** action before the action that causes the dialog box to open and set the **Wait** argument to **No**.</span></span>
> - <span data-ttu-id="10abc-p105">Il est parfois difficile d'estimer le temps qu'il faudra à la séquence de touches pour atteindre Access ou une autre application. En conséquence, lorsqu'il existe une autre méthode (telle que l'action **TrouverEnregistrement** ) pour effectuer la tâche souhaitée, il est conseillé d'utiliser cette méthode au lieu de l'action **EnvoiTouches** pour compléter les options d'une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="10abc-p105">The timing of the keystrokes reaching Access or another application can be tricky. As a result, it's recommended that if there's some other method (such as the **FindRecord** action) you can use to achieve a desired task, use that method rather than using the **SendKeys** action to fill in the options in a dialog box.</span></span>

<span data-ttu-id="10abc-133">Si vous voulez envoyer plus de 255 caractères à Access ou à une autre application Windows, vous pouvez utiliser successivement plusieurs actions **EnvoiTouches** dans une macro.</span><span class="sxs-lookup"><span data-stu-id="10abc-133">If you want to send more than 255 characters to Access or another Windows-based application, you can use several **SendKeys** actions in succession in a macro.</span></span>

<span data-ttu-id="10abc-p106">Le recours à l'action **EnvoiTouches** pour envoyer une séquence de touches déclenche les événements **KeyDown**, **KeyUp** et **KeyPress** appropriés. L'envoi d'une séquence de touches non-ANSI (une touche de fonction, par exemple) ne déclenche pas l'événement **KeyPress**.</span><span class="sxs-lookup"><span data-stu-id="10abc-p106">Using the **SendKeys** action to send keystrokes triggers the appropriate **KeyDown**, **KeyUp**, and **KeyPress** events. Sending non-ANSI keystrokes (such as a function key) doesn't trigger the **KeyPress** event.</span></span>

<span data-ttu-id="10abc-p107">Cette action n'est pas disponible à partir d'un module Visual Basic pour Applications (VBA). Utilisez dans ce cas l'instruction **SendKeys**.</span><span class="sxs-lookup"><span data-stu-id="10abc-p107">This action isn't available from a Visual Basic for Applications (VBA) module. Use the **SendKeys** statement instead.</span></span>

