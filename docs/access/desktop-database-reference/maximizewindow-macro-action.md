---
title: AgrandirFenêtre, action de macro
TOCTitle: MaximizeWindow Macro Action
ms:assetid: 79c9e430-07a7-02b2-ff5a-c6b9ec32c5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196171(v=office.15)
ms:contentKeyID: 48545778
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm196948
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b612d050d6c523ae836b21aa27826ff180e8f977
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470566"
---
# <a name="maximizewindow-macro-action"></a><span data-ttu-id="c0684-102">AgrandirFenêtre, action de macro</span><span class="sxs-lookup"><span data-stu-id="c0684-102">MaximizeWindow Macro Action</span></span>


<span data-ttu-id="c0684-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0684-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c0684-104">Si Access est configuré pour utiliser des fenêtres superposées au lieu des documents à onglets, vous pouvez utiliser l’action **Agrandirfenêtre** pour agrandir la fenêtre active afin qu’elle remplisse la fenêtre Access.</span><span class="sxs-lookup"><span data-stu-id="c0684-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MaximizeWindow** action to enlarge the active window so that it fills the Access window.</span></span> <span data-ttu-id="c0684-105">Cette action vous permet de voir la plus grande partie possible de l'objet dans la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="c0684-105">This action will allow you to see as much of the object in the active window as possible.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c0684-p102">[!REMARQUE] Cette action ne peut être appliquée aux fenêtres de code dans Visual Basic Editor. Pour plus d'informations sur la façon d'affecter des fenêtres de code, reportez-vous à la rubrique relative à la propriété <STRONG>WindowState</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="c0684-p102">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the <STRONG>WindowState</STRONG> property topic.</span></span></P>



## <a name="setting"></a><span data-ttu-id="c0684-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0684-108">Setting</span></span>

<span data-ttu-id="c0684-109">L'action **AgrandirFenêtre** ne possède aucun argument.</span><span class="sxs-lookup"><span data-stu-id="c0684-109">The **MaximizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0684-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="c0684-110">Remarks</span></span>

<span data-ttu-id="c0684-111">Cette action équivaut à cliquer sur le bouton **Agrandir** dans le coin supérieur droit de la fenêtre ou à cliquer sur **Agrandir** dans le menu **Contrôle** de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c0684-111">This action has the same effect as clicking the **Maximize** button in the window's upper-right corner or clicking **Maximize** on the window's **Control** menu.</span></span>

<span data-ttu-id="c0684-112">Vous pouvez utiliser l'action **RestaurerFenêtre** pour rétablir la taille initiale de la fenêtre agrandie.</span><span class="sxs-lookup"><span data-stu-id="c0684-112">You can use the **RestoreWindow** action to restore a maximized window to its previous size.</span></span>

<span data-ttu-id="c0684-113">**Conseils**</span><span class="sxs-lookup"><span data-stu-id="c0684-113">**Tips**</span></span>

  - <span data-ttu-id="c0684-114">Vous devrez peut-être utiliser la méthode **SélectionnerObjet** si la fenêtre que vous voulez agrandir n'est pas la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="c0684-114">You may need to use the **SelectObject** action if the window you want to maximize isn't the active window.</span></span>

  - <span data-ttu-id="c0684-p103">Si vous agrandissez une fenêtre dans Microsoft Access, toutes les autres fenêtres sont également agrandies lors de leur ouverture ou de leur activation. Cependant, la taille des formulaires indépendants reste inchangée. Pour qu'un formulaire conserve sa taille d'origine lorsque vous agrandissez d'autres fenêtres, attribuez la valeur **Oui** à sa propriété **FenIndépendante**.</span><span class="sxs-lookup"><span data-stu-id="c0684-p103">When you maximize a window in Access, all other windows are also maximized when you open them or switch to them. However, pop-up forms aren't maximized. If you want a form to maintain its size when other windows are maximized, set its **PopUp** property to **Yes**.</span></span>

<span data-ttu-id="c0684-118">Pour exécuter l'action **AgrandirFenêtre** dans un module Visual Basic pour Applications, utilisez la méthode **Maximize** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="c0684-118">To run the **MaximizeWindow** action in a Visual Basic for Applications module, use the **Maximize** method of the **DoCmd** object.</span></span>

