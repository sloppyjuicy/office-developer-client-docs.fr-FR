---
title: FindNextRecord, action de macro
TOCTitle: FindNextRecord macro action
ms:assetid: 57fb6457-9098-4e81-c693-78ccd262ce0b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194307(v=office.15)
ms:contentKeyID: 48544985
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89832
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 426bf296345c47abe58e3e6e5057a43a0d43aa21
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936629"
---
# <a name="findnextrecord-macro-action"></a><span data-ttu-id="6653c-102">FindNextRecord, action de macro</span><span class="sxs-lookup"><span data-stu-id="6653c-102">FindNextRecord macro action</span></span>


<span data-ttu-id="6653c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6653c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6653c-p101">Utilisez l'action **RechercherEnregistrementSuivant** pour trouver l'enregistrement suivant qui répond aux critères spécifiés par l'action **TrouverEnregistrement** précédente ou par la valeur de la boîte de dialogue **Rechercher et remplacer** (sous l'onglet **Accueil**, cliquez sur **Rechercher**). Vous pouvez également utiliser l'action **RechercherEnregistrementSuivant** pour rechercher un à un des enregistrements, par exemple des enregistrements relatifs à un client spécifique.</span><span class="sxs-lookup"><span data-stu-id="6653c-p101">You can use the **FindNextRecord** action to find the next record that meets the criteria specified by the previous **FindRecord** action or the value in the **Find and Replace** dialog box (on the **Home** tab, click **Find**). You can use the **FindNextRecord** action to search repeatedly for records. For example, you can move successively through all the records for a specific customer.</span></span>

## <a name="setting"></a><span data-ttu-id="6653c-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="6653c-107">Setting</span></span>

<span data-ttu-id="6653c-108">L’action **Rechercherenregistrementsuivant** ne possède aucun argument.</span><span class="sxs-lookup"><span data-stu-id="6653c-108">The **FindNextRecord** action doesn't have any arguments.</span></span> <span data-ttu-id="6653c-109">L’action **Rechercherenregistrementsuivant** recherche l’enregistrement suivant qui répond aux critères définis par l’action **TrouverEnregistrement** ou dans la boîte de dialogue **Rechercher et remplacer** .</span><span class="sxs-lookup"><span data-stu-id="6653c-109">The **FindNextRecord** action finds the next record that meets the criteria set either by the **FindRecord** action or in the **Find and Replace** dialog box.</span></span> <span data-ttu-id="6653c-110">Les arguments de l’action **TrouverEnregistrement** sont partagés avec les options dans la boîte de dialogue **Rechercher et remplacer** .</span><span class="sxs-lookup"><span data-stu-id="6653c-110">The arguments for the **FindRecord** action are shared with the options in the **Find and Replace** dialog box.</span></span>

<span data-ttu-id="6653c-p103">Pour définir les critères de recherche, utilisez l'action **TrouverEnregistrement**. Généralement, vous entrez une action **TrouverEnregistrement** dans une macro, puis utilisez l'action **RechercherEnregistrementSuivant** pour rechercher un à un les enregistrements répondant aux mêmes critères. Pour rechercher des enregistrements uniquement lorsqu'une certaine condition est remplie, vous pouvez entrer une expression conditionnelle dans la colonne **Condition** de la ligne correspondant à l'action **RechercherEnregistrementSuivant**.</span><span class="sxs-lookup"><span data-stu-id="6653c-p103">To set the search criteria, use the **FindRecord** action. Typically, you enter a **FindRecord** action in a macro and then use the **FindNextRecord** action to find succeeding records that meet the same criteria. To search for records only when a certain condition is met, you can enter a conditional expression in the **Condition** column of the action row for the **FindNextRecord** action.</span></span>

## <a name="remarks"></a><span data-ttu-id="6653c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6653c-114">Remarks</span></span>

<span data-ttu-id="6653c-115">Cette action équivaut à utiliser le bouton **Suivant** dans la boîte de dialogue **Rechercher et remplacer**.</span><span class="sxs-lookup"><span data-stu-id="6653c-115">This action has the same effect as using the **Find Next** button in the **Find and Replace** dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="6653c-p104">[!REMARQUE] Bien que l'action **TrouverEnregistrement** corresponde à la commande **Rechercher** de l'onglet **Accueil** pour les tables, requêtes et formulaires, elle ne correspond pas à la commande **Rechercher** du menu **Edition** dans la fenêtre Code. Vous ne pouvez pas utiliser l'action **TrouverEnregistrement** ni l'action **RechercherEnregistrementSuivant** pour rechercher du texte dans des modules.</span><span class="sxs-lookup"><span data-stu-id="6653c-p104">Although the **FindRecord** action corresponds to the **Find** command on the **Home** tab for tables, queries, and forms, it doesn't correspond to the **Find** command on the **Edit** menu in the Code window. You can't use the **FindRecord** action or **FindNextRecord** action to search for text in modules.</span></span>

> [!TIP]
> <span data-ttu-id="6653c-118">[!CONSEIL] Si vous avez défini l'argument **Champ actif uniquement** de l'action **TrouverEnregistrement** sur **Oui**, vous devrez peut-être utiliser l'action **AtteindreContrôle** pour déplacer le focus sur le contrôle contenant les données que vous recherchez avant d'utiliser l'action **RechercherEnregistrementSuivant**.</span><span class="sxs-lookup"><span data-stu-id="6653c-118">If you've set the **Only Current Field** argument of the **FindRecord** action to **Yes**, you may need to use the **GoToControl** action to move the focus to the control containing the data you're searching for before you use the **FindNextRecord** action.</span></span>

<span data-ttu-id="6653c-p105">Si le texte actuellement sélectionné correspond au texte recherché au moment de l'exécution de l'action de macro **RechercherEnregistrementSuivant**, la recherche commence immédiatement après la sélection, dans le même champ que la sélection et dans le même enregistrement. Sinon, la recherche commence au début de l'enregistrement actif. Cela vous permet de rechercher plusieurs instances des mêmes critères de recherche dans un même enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6653c-p105">If the currently selected text is the same as the search text at the time the **FindNextRecord** macro action is carried out, the search begins immediately following the selection, in the same field as the selection, and in the same record. Otherwise, the search begins at the start of the current record. This enables you to find multiple instances of the same search criteria that might appear in a single record.</span></span>

<span data-ttu-id="6653c-p106">Notez toutefois que si vous utilisez un bouton de commande pour exécuter une macro contenant l'action **RechercherEnregistrementSuivant**, la première instance des critères de recherche sera trouvée en boucle. En effet, le fait de cliquer sur le bouton de commande supprime le focus du champ contenant la valeur correspondante. L'action **RechercherEnregistrementSuivant** commencera la recherche au début de l'enregistrement. Pour éviter cela, exécutez la macro à l'aide d'une technique qui ne modifie pas le focus, comme un bouton de barre d'outils personnalisé ou une combinaison de touches définie dans une macro AutoKeys. Vous pouvez également définir le focus dans la macro sur le champ contenant les critères de recherche avant d'exécuter l'action **RechercherEnregistrementSuivant**.</span><span class="sxs-lookup"><span data-stu-id="6653c-p106">However, note that if you use a command button to run a macro containing the **FindNextRecord** action, the first instance of the search criteria will be found repeatedly. This behavior occurs because clicking the command button removes the focus from the field containing the matching value. The **FindNextRecord** action will then begin searching from the start of the record. To avoid this problem, run the macro by using a technique that doesn't change the focus, such as a custom toolbar button or a key combination defined in an AutoKeys macro. Alternatively, set the focus in the macro to the field containing the search criteria before you carry out the **FindNextRecord** action.</span></span>

<span data-ttu-id="6653c-127">Ce comportement est également observé si vous utilisez un bouton de commande pour exécuter une macro contenant l'action **TrouverEnregistrement** avec l'argument **Trouver le premier** défini sur **Non**.</span><span class="sxs-lookup"><span data-stu-id="6653c-127">The same behavior also occurs if you use a command button to run a macro containing the **FindRecord** action with the **Find First** argument set to **No**.</span></span>

<span data-ttu-id="6653c-128">Pour exécuter l'action **RechercherEnregistrementSuivant** dans un module Visual Basic pour Applications, utilisez la méthode **FindNext** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="6653c-128">To run the **FindNextRecord** action in a Visual Basic for Applications module, use the **FindNext** method of the **DoCmd** object.</span></span>

