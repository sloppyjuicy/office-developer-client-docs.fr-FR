---
title: Boîte de dialogue des propriétés personnalisées du contrôle ActiveX
TOCTitle: ActiveX Control's Custom Properties Dialog Box
ms:assetid: 124cf679-6efc-567a-84d1-8057dec93bde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15)
ms:contentKeyID: 48543338
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm4040
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6f5924d04e9ea4febee1434f6ef99f95b02eab6b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471091"
---
# <a name="activex-controls-custom-properties-dialog-box"></a><span data-ttu-id="c9cb3-102">Boîte de dialogue des propriétés personnalisées du contrôle ActiveX</span><span class="sxs-lookup"><span data-stu-id="c9cb3-102">ActiveX Control's Custom Properties Dialog Box</span></span>

<span data-ttu-id="c9cb3-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9cb3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c9cb3-p101">Lors de la définition des propriétés d'un contrôle ActiveX, vous devrez ou souhaiterez peut-être utiliser la boîte de dialogue des propriétés personnalisée du contrôle. Cette boîte de dialogue des propriétés personnalisée propose une alternative à la liste des propriétés figurant dans la feuille des propriétés Microsoft Access pour définir les propriétés d'un contrôle ActiveX en mode Création de formulaire.</span><span class="sxs-lookup"><span data-stu-id="c9cb3-p101">When setting the properties of an ActiveX control, you may need or prefer to use the control's custom properties dialog box. This custom properties dialog box provides an alternative to the list of properties in the Microsoft Access property sheet for setting ActiveX control properties in Design view.</span></span>

> [!NOTE]
> <span data-ttu-id="c9cb3-106">[!REMARQUE] Ces informations s'appliquent uniquement aux contrôles ActiveX dans un environnement de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c9cb3-106">This information only applies to ActiveX controls in a Microsoft Access database environment.</span></span>



## <a name="two-ways-to-set-properties"></a><span data-ttu-id="c9cb3-107">Deux manières de définir des propriétés</span><span class="sxs-lookup"><span data-stu-id="c9cb3-107">Two Ways to Set Properties</span></span>

<span data-ttu-id="c9cb3-p102">La raison d'être de la boîte de dialogue des propriétés personnalisée est que toutes les applications qui utilisent des contrôles ActiveX ne fournissent pas une feuille des propriétés comme Microsoft Access. La boîte de dialogue des propriétés personnalisée fournit une interface pour la définition des propriétés clés du contrôle sans tenir compte de l'interface fournie par l'application hôte.</span><span class="sxs-lookup"><span data-stu-id="c9cb3-p102">The reason for the custom properties dialog box is that not all applications that use ActiveX controls provide a property sheet like the one in Microsoft Access. The custom properties dialog box provides an interface for setting key control properties regardless of the interface supplied by the hosting application.</span></span>

<span data-ttu-id="c9cb3-110">Pour certaines propriétés de contrôle ActiveX, vous pouvez choisir un des deux endroits suivants pour définir la propriété :</span><span class="sxs-lookup"><span data-stu-id="c9cb3-110">For some ActiveX control properties, you can choose either of these two locations to set the property:</span></span>

  - <span data-ttu-id="c9cb3-111">La feuille des propriétés Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c9cb3-111">The Microsoft Access property sheet.</span></span>

  - <span data-ttu-id="c9cb3-112">La boîte de dialogue des propriétés personnalisée du contrôle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="c9cb3-112">The ActiveX control's custom properties dialog box.</span></span>

<span data-ttu-id="c9cb3-p103">Dans certains cas, la boîte de dialogue des propriétés personnalisée est la seule manière de définir une propriété en mode Création. Cela est généralement le cas lorsque l'interface nécessaire pour définir une propriété ne fonctionne pas avec la feuille des propriétés de Microsoft Access. Par exemple, la propriété **GridFont** du contrôle Calendrier dispose d'un certain nombre d'éléments, mais vous ne pouvez en définir qu'un seul par propriété à l'aide de la feuille des propriétés de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c9cb3-p103">In some cases, the custom properties dialog box is the only way to set a property in Design view. This is usually the situation when the interface needed to set a property doesn't work inside the Microsoft Access property sheet. For example, the **GridFont** property for the Calendar control has a number of arguments; you can't set more than one argument per property in the Microsoft Access property sheet.</span></span>

## <a name="finding-the-custom-properties-dialog-box"></a><span data-ttu-id="c9cb3-116">Recherche de la boîte de dialogue des propriétés personnalisée</span><span class="sxs-lookup"><span data-stu-id="c9cb3-116">Finding the Custom Properties Dialog Box</span></span>

<span data-ttu-id="c9cb3-p104">Tous les contrôles ActiveX ne fournissent pas une boîte de dialogue des propriétés personnalisée. Pour voir si un contrôle fournit cette boîte de dialogue des propriétés personnalisée, recherchez la propriété **Personnalisé** de ce contrôle dans la feuille des propriétés de Microsoft Access. Si la liste des propriétés contient le nom **Personnalisé**, cela signifie que le contrôle fournit la boîte de dialogue des propriétés personnalisée.</span><span class="sxs-lookup"><span data-stu-id="c9cb3-p104">Not all ActiveX controls provide a custom properties dialog box. To see whether a control provides this custom properties dialog box, look for the **Custom** property in the Microsoft Access property sheet for this control. If the list of properties contains the name **Custom**, then the control provides the custom properties dialog box.</span></span>

## <a name="using-the-custom-properties-dialog-box"></a><span data-ttu-id="c9cb3-120">Utilisation de la boîte de dialogue des propriétés personnalisée</span><span class="sxs-lookup"><span data-stu-id="c9cb3-120">Using the Custom Properties Dialog Box</span></span>

<span data-ttu-id="c9cb3-p105">Après avoir cliqué dans la zone de propriété **Personnalisé** de la feuille des propriétés de Microsoft Access, cliquez sur le bouton **Générer** à droite de la zone des propriétés pour afficher la boîte de dialogue des propriétés personnalisée du contrôle, qui apparaît souvent sous la forme d'une boîte de dialogue comportant des onglets. Choisissez l'onglet contenant l'interface permettant de définir les propriétés souhaitées.</span><span class="sxs-lookup"><span data-stu-id="c9cb3-p105">After you click the **Custom** property box in the Microsoft Access property sheet, click the **Build** button to the right of the property box to display the control's custom properties dialog box, often presented as a tabbed dialog box. Choose the tab that contains the interface for setting the properties that you want to set.</span></span>

<span data-ttu-id="c9cb3-p106">Le plus souvent, après avoir effectué les changements dans un onglet, vous pouvez les appliquer immédiatement en cliquant sur le bouton **Appliquer** (s'il est fourni). Vous pouvez cliquer sur les autres onglets pour définir les autres propriétés. Pour approuver tous les changements effectués dans la boîte de dialogue des propriétés personnalisée, cliquez sur le bouton **OK**. Pour retourner à la feuille des propriétés de Microsoft Access sans modification, cliquez sur le bouton **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="c9cb3-p106">After you make changes on one tab, you can often apply those changes immediately by clicking the **Apply** button (if provided). You can click other tabs to set other properties as needed. To approve all changes made in the custom properties dialog box, click the **OK** button. To return to the Microsoft Access property sheet without changing any property settings, click the **Cancel** button.</span></span>

<span data-ttu-id="c9cb3-p107">Vous pouvez afficher la boîte de dialogue des propriétés personnalisée en cliquant sur la sous-commande **Propriétés** de la commande **Objet** du contrôle ActiveX (par exemple, **Contrôle Calendrier**) dans le menu **Edition** ou en cliquant sur la même sous-commande du menu contextuel du contrôle ActiveX. De plus, certaines propriétés dans la feuille des propriétés de Microsoft Access du contrôle ActiveX, comme la propriété **GridFontColor** du contrôle Calendrier, disposent d'un bouton **Générer** à droite de la zone des propriétés. Lorsque vous cliquez sur le bouton **Générer**, la boîte de dialogue des propriétés personnalisée s'affiche avec les onglets appropriés sélectionnés (par exemple, l'onglet **Couleurs**).</span><span class="sxs-lookup"><span data-stu-id="c9cb3-p107">You can also view the custom properties dialog box by clicking the **Properties** subcommand of the ActiveX control **Object** command (for example, **Calendar Control Object**) on the **Edit** menu, or by clicking this same subcommand on the shortcut menu for the ActiveX control. In addition, some properties in the Microsoft Access property sheet for the ActiveX control, like the **GridFontColor** property of the Calendar control, have a **Build** button to the right of the property box. When you click the **Build** button, the custom properties dialog box is displayed, with the appropriate tab selected (for example, **Colors**).</span></span>

