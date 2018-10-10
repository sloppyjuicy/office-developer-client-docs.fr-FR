---
title: AnnulerEvénement, action de macro
TOCTitle: CancelEvent Macro Action
ms:assetid: d9d3ea99-c9fb-2524-c570-e3ee6d20af98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835110(v=office.15)
ms:contentKeyID: 48548066
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm78430
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 52822d45b30c631dcabe3c38b6722398e96f489f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471641"
---
# <a name="cancelevent-macro-action"></a><span data-ttu-id="bf320-102">AnnulerEvénement, action de macro</span><span class="sxs-lookup"><span data-stu-id="bf320-102">CancelEvent Macro Action</span></span>


<span data-ttu-id="bf320-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf320-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="bf320-104">Vous pouvez utiliser l’action **AnnulerEvénement** pour annuler l’événement qui a provoqué l’accès exécuter la macro contenant cette action.</span><span class="sxs-lookup"><span data-stu-id="bf320-104">You can use the **CancelEvent** action to cancel the event that caused Access to run the macro containing this action.</span></span> <span data-ttu-id="bf320-105">Le nom de la macro est le paramètre d'une propriété de type événement comme **AvantMAJ**, **SurOuverture**, **SurLibération** ou **SurImpression**.</span><span class="sxs-lookup"><span data-stu-id="bf320-105">The macro name is the setting of an event property such as **BeforeUpdate**, **OnOpen**, **OnUnload**, or **OnPrint**.</span></span>

## <a name="setting"></a><span data-ttu-id="bf320-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf320-106">Setting</span></span>

<span data-ttu-id="bf320-107">L'action **AnnulerEvénement** ne possède aucun argument.</span><span class="sxs-lookup"><span data-stu-id="bf320-107">The **CancelEvent** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf320-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="bf320-108">Remarks</span></span>

<span data-ttu-id="bf320-p102">Dans un formulaire, l'action **AnnulerEvénement** est généralement utilisée dans une macro de validation avec la propriété de type événement **AvantMAJ**. Lorsqu'un utilisateur entre des données dans un contrôle ou un enregistrement, Access exécute la macro avant d'ajouter les données dans la base de données. Si ces données ne répondent pas aux conditions de validation de la macro, l'action **AnnulerÉvénement** annule le processus de mise à jour avant même qu'il ne débute.</span><span class="sxs-lookup"><span data-stu-id="bf320-p102">In a form, you typically use the **CancelEvent** action in a validation macro with the **BeforeUpdate** event property. When a user enters data in a control or record, Access runs the macro before adding the data to the database. If the data fails the validation conditions in the macro, the **CancelEvent** action cancels the update process before it starts.</span></span>

<span data-ttu-id="bf320-112">Cette action est souvent utilisée avec l'action **ZoneMessage** pour indiquer que les données n'ont pas rempli les conditions de validation et pour fournir des informations utiles sur le genre de données qui doit être entré.</span><span class="sxs-lookup"><span data-stu-id="bf320-112">Often, you use this action with the **MessageBox** action to indicate that the data has failed the validation conditions and to provide helpful information about the kind of data that should be entered.</span></span>

<span data-ttu-id="bf320-113">Les événements suivants peuvent être annulés par l'action **AnnulerEvénement**.</span><span class="sxs-lookup"><span data-stu-id="bf320-113">The following events can be canceled by the **CancelEvent** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf320-114"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="bf320-114"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="bf320-115"><strong>Dirty</strong></span><span class="sxs-lookup"><span data-stu-id="bf320-115"><strong>Dirty</strong></span></span></p></td>
<td><p><span data-ttu-id="bf320-116"><strong>MouseDown</strong></span><span class="sxs-lookup"><span data-stu-id="bf320-116"><strong>MouseDown</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf320-117"><strong>BeforeDelConfirm</strong></span><span class="sxs-lookup"><span data-stu-id="bf320-117"><strong>BeforeDelConfirm</strong></span></span></p></td>
<td><p><span data-ttu-id="bf320-118"><strong>Exit</strong></span><span class="sxs-lookup"><span data-stu-id="bf320-118"><strong>Exit</strong></span></span></p></td>
<td><p><span data-ttu-id="bf320-119"><strong>NoData</strong></span><span class="sxs-lookup"><span data-stu-id="bf320-119"><strong>NoData</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf320-120"><strong>BeforeInsert</strong></span><span class="sxs-lookup"><span data-stu-id="bf320-120"><strong>BeforeInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="bf320-121"><strong>Filter</strong></span><span class="sxs-lookup"><span data-stu-id="bf320-121"><strong>Filter</strong></span></span></p></td>
<td><p><span data-ttu-id="bf320-122"><strong>Open</strong></span><span class="sxs-lookup"><span data-stu-id="bf320-122"><strong>Open</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf320-123"><strong>BeforeUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="bf320-123"><strong>BeforeUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="bf320-124"><strong>Format</strong></span><span class="sxs-lookup"><span data-stu-id="bf320-124"><strong>Format</strong></span></span></p></td>
<td><p><span data-ttu-id="bf320-125"><strong>Print</strong></span><span class="sxs-lookup"><span data-stu-id="bf320-125"><strong>Print</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf320-126"><strong>DblClick</strong></span><span class="sxs-lookup"><span data-stu-id="bf320-126"><strong>DblClick</strong></span></span></p></td>
<td><p><span data-ttu-id="bf320-127"><strong>KeyPress</strong></span><span class="sxs-lookup"><span data-stu-id="bf320-127"><strong>KeyPress</strong></span></span></p></td>
<td><p><span data-ttu-id="bf320-128"><strong>Unload</strong></span><span class="sxs-lookup"><span data-stu-id="bf320-128"><strong>Unload</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf320-129"><strong>Supprimer</strong></span><span class="sxs-lookup"><span data-stu-id="bf320-129"><strong>Delete</strong></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="bf320-130">[!REMARQUE] Vous pouvez utiliser l'action <STRONG>AnnulerEvénement</STRONG> avec l'événement <STRONG>SourisAppuyée</STRONG> uniquement pour annuler l'événement qui est déclenché lorsque vous cliquez avec le bouton droit sur un objet.</span><span class="sxs-lookup"><span data-stu-id="bf320-130">You can use the <STRONG>CancelEvent</STRONG> action with the <STRONG>MouseDown</STRONG> event only to cancel the event that occurs when you right-click an object.</span></span></P>



<span data-ttu-id="bf320-131">Si le paramètre de la propriété de type événement **SurDoubleClic** d'un contrôle spécifie une macro contenant l'action **AnnulerEvénement**, l'action annule l'événement **DoubleClic**.</span><span class="sxs-lookup"><span data-stu-id="bf320-131">If a control's **OnDblClick** event property setting specifies a macro containing the **CancelEvent** action, the action cancels the **DblClick** event.</span></span>

<span data-ttu-id="bf320-p103">Le comportement par défaut des événements pouvant être annulés (à savoir, le comportement d'Access lorsque l'événement est déclenché) a lieu une fois la macro événementielle exécutée. Ceci vous permet d'annuler le comportement par défaut. Par exemple, lorsque vous double-cliquez sur un mot sur lequel se trouve le point d'insertion dans une zone de texte, Access sélectionne normalement ce mot. Vous pouvez, cependant, annuler ce comportement par défaut dans la macro événementielle **DoubleClic** et exécuter une autre action comme l'ouverture d'un formulaire contenant des informations sur le contenu de la zone de texte. Le comportement par défaut des événements ne pouvant pas être annulés a lieu avant l'exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="bf320-p103">For events that can be canceled, the default behavior for the event (that is, what Access typically does when the event occurs) occurs after the macro for the event runs. This enables you to cancel the default behavior. For example, when you double-click a word that the insertion point is on in a text box, Access normally selects the word. You can cancel this default behavior in the macro for the **DblClick** event and perform some other action, such as opening a form containing information about the data in the text box. For events that can't be canceled, the default behavior occurs before the macro runs.</span></span>


> [!NOTE]
> <P><span data-ttu-id="bf320-p104">[!REMARQUE] Si la propriété de type événement <STRONG>SurLibération</STRONG> d'un formulaire spécifie une macro qui exécute une action <STRONG>AnnulerEvénement</STRONG>, vous ne pourrez pas fermer le formulaire. Vous devez soit corriger la condition à l'origine de l'exécution de l'action <STRONG>AnnulerEvénement</STRONG>, soit ouvrir la macro et supprimer l'action <STRONG>AnnulerEvénement</STRONG>. Si le formulaire est un formulaire modal, vous ne pourrez pas ouvrir la macro.</span><span class="sxs-lookup"><span data-stu-id="bf320-p104">If a form's <STRONG>OnUnload</STRONG> event property specifies a macro that carries out a <STRONG>CancelEvent</STRONG> action, you won't be able to close the form. You must either correct the condition that caused the <STRONG>CancelEvent</STRONG> action to be carried out or open the macro and delete the <STRONG>CancelEvent</STRONG> action. If the form is a modal form, you won't be able to open the macro.</span></span></P>



<span data-ttu-id="bf320-140">Pour exécuter l'action **AnnulerEvénement** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **CancelEvent** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="bf320-140">To carry out the **CancelEvent** action in a Visual Basic for Applications (VBA) module, use the **CancelEvent** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="bf320-141">Exemple</span><span class="sxs-lookup"><span data-stu-id="bf320-141">Example</span></span>

<span data-ttu-id="bf320-142"> Valider des données à l’aide d’une macro</span><span class="sxs-lookup"><span data-stu-id="bf320-142">Validate data by using a macro</span></span>

<span data-ttu-id="bf320-p105">La macro de validation suivante vérifie les codes postaux entrés dans un formulaire Fournisseurs. Elle illustre l'utilisation des actions **ArrêtMacro**, **ZoneMessage**, **AnnulerEvénement** et **AtteindreContrôle**. Une expression conditionnelle vérifie le pays/la région et le code postal entrés dans un enregistrement du formulaire. Si le code postal n'est pas dans le format correct pour le pays/la région, la macro affiche une zone de message et annule la sauvegarde de l'enregistrement. Elle vous renvoie ensuite au contrôle Code postal où vous pouvez corriger l'erreur. Cette macro doit être attachée à la propriété **AvantMAJ** du formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="bf320-p105">The following validation macro checks the postal codes entered in a Suppliers form. It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions. A conditional expression checks the country/region and postal code entered in a record on the form. If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record. It then returns you to the Postal Code control, where you can correct the error. This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bf320-149">Condition</span><span class="sxs-lookup"><span data-stu-id="bf320-149">Condition</span></span></p></th>
<th><p><span data-ttu-id="bf320-150">Action</span><span class="sxs-lookup"><span data-stu-id="bf320-150">Action</span></span></p></th>
<th><p><span data-ttu-id="bf320-151">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="bf320-151">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="bf320-152">Commentaire</span><span class="sxs-lookup"><span data-stu-id="bf320-152">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf320-153">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="bf320-153">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="bf320-154">StopMacro</span><span class="sxs-lookup"><span data-stu-id="bf320-154">StopMacro</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="bf320-155">Si PaysRégion est <strong>Null</strong>, le code postal ne peut pas être validé.</span><span class="sxs-lookup"><span data-stu-id="bf320-155">If CountryRegion is <strong>Null</strong>, postal code can't be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf320-156">[PaysRégion] Dans (&quot;France&quot;,&quot;Italie&quot;,&quot;Espagne&quot;) et NBCAR ([Code Postal]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="bf320-156">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([Postal Code]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="bf320-157">MessageBox</span><span class="sxs-lookup"><span data-stu-id="bf320-157">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="bf320-158">Message : Le code postal doit contenir 5 caractères. 

</span><span class="sxs-lookup"><span data-stu-id="bf320-158">Message: The postal code must be 5 characters.</span></span> <span data-ttu-id="bf320-159">Bip : <strong>Oui</strong> Type : <strong>informations</strong> titre : Code Postal erroné</span><span class="sxs-lookup"><span data-stu-id="bf320-159">Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="bf320-160">Si le code postal ne contient pas 5 caractères, affiche un message.</span><span class="sxs-lookup"><span data-stu-id="bf320-160">If the postal code isn't 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf320-161">...</span><span class="sxs-lookup"><span data-stu-id="bf320-161"></span></span></p></td>
<td><p><span data-ttu-id="bf320-162">CancelEvent</span><span class="sxs-lookup"><span data-stu-id="bf320-162">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="bf320-163">Annule l’événement.</span><span class="sxs-lookup"><span data-stu-id="bf320-163">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="bf320-164">GoToControl</span><span class="sxs-lookup"><span data-stu-id="bf320-164">GoToControl</span></span></p></td>
<td><p><span data-ttu-id="bf320-165">Nom du contrôle : CodePostal</span><span class="sxs-lookup"><span data-stu-id="bf320-165">Control Name: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf320-166">[PaysRégion] Dans (&quot;Australie&quot;,&quot;Singapour&quot;) et NBCAR ([Code Postal]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="bf320-166">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([Postal Code]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="bf320-167">MessageBox</span><span class="sxs-lookup"><span data-stu-id="bf320-167">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="bf320-168">Message : Le code postal doit contenir 4 caractères. 

</span><span class="sxs-lookup"><span data-stu-id="bf320-168">Message: The postal code must be 4 characters.</span></span> <span data-ttu-id="bf320-169">Bip : <strong>Oui</strong> Type : <strong>informations</strong> titre : Code Postal erroné</span><span class="sxs-lookup"><span data-stu-id="bf320-169">Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="bf320-170">Si le code postal ne contient pas 4 caractères, affiche un message.</span><span class="sxs-lookup"><span data-stu-id="bf320-170">If the postal code isn't 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf320-171">...</span><span class="sxs-lookup"><span data-stu-id="bf320-171"></span></span></p></td>
<td><p><span data-ttu-id="bf320-172">CancelEvent</span><span class="sxs-lookup"><span data-stu-id="bf320-172">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="bf320-173">Annule l’événement.</span><span class="sxs-lookup"><span data-stu-id="bf320-173">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="bf320-174">GoToControl</span><span class="sxs-lookup"><span data-stu-id="bf320-174">GoToControl</span></span></p></td>
<td><p><span data-ttu-id="bf320-175">Nom du contrôle : CodePostal</span><span class="sxs-lookup"><span data-stu-id="bf320-175">Control Name: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf320-176">([PaysRégion] = &quot;Canada&quot;) Et ([Code Postal] pas comme&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</span><span class="sxs-lookup"><span data-stu-id="bf320-176">([CountryRegion] = &quot;Canada&quot;) And ([Postal Code] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="bf320-177">MessageBox</span><span class="sxs-lookup"><span data-stu-id="bf320-177">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="bf320-178">Message : Le code postal n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="bf320-178">Message: The postal code is not valid.</span></span> <span data-ttu-id="bf320-179">Exemple de code canadien : H1J 1C3 bip : <strong>Oui</strong> Type : titre des <strong>informations</strong> : erreur de Code Postal</span><span class="sxs-lookup"><span data-stu-id="bf320-179">Example of Canadian code: H1J 1C3 Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="bf320-p109">Si le code postal n’est pas correct pour le Canada, affiche un message. (Exemple de code postal canadien : H1J 1C3.)</span><span class="sxs-lookup"><span data-stu-id="bf320-p109">If the postal code isn't correct for Canada, display a message. (Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf320-182">...</span><span class="sxs-lookup"><span data-stu-id="bf320-182"></span></span></p></td>
<td><p><span data-ttu-id="bf320-183">CancelEvent</span><span class="sxs-lookup"><span data-stu-id="bf320-183">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="bf320-184">Annule l’événement.</span><span class="sxs-lookup"><span data-stu-id="bf320-184">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

