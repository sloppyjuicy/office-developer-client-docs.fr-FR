---
title: Création d'un contrôle ActiveX pouvant lier des données de formulaire InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0d62047-bf08-9f70-de00-7f81ef1331f1
description: Vous pouvez héberger des contrôles ActiveX dans les formulaires InfoPath qui sont conçus pour être ouverts dans l'éditeur InfoPath. Ces contrôles peuvent être créés au préalable (avec certaines contraintes) ou ils peuvent être écrits spécialement pour InfoPath.
ms.openlocfilehash: 70ac6a16b305403ffa99d8fe840a165913642f57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300188"
---
# <a name="create-an-activex-control-that-can-bind-to-infopath-form-data"></a><span data-ttu-id="ea62b-104">Création d'un contrôle ActiveX pouvant lier des données de formulaire InfoPath</span><span class="sxs-lookup"><span data-stu-id="ea62b-104">Create an ActiveX Control that can Bind to InfoPath Form Data</span></span>

<span data-ttu-id="ea62b-p102">Vous pouvez héberger des contrôles ActiveX dans les formulaires InfoPath qui sont conçus pour être ouverts dans l'éditeur InfoPath. Ces contrôles peuvent être créés au préalable (avec certaines contraintes) ou ils peuvent être écrits spécialement pour InfoPath.</span><span class="sxs-lookup"><span data-stu-id="ea62b-p102">You can host ActiveX controls in InfoPath forms that are designed to be opened in the InfoPath editor. These controls can be preexisting (with some constraints) or can be written specifically for InfoPath.</span></span>
  
## <a name="write-an-activex-control"></a><span data-ttu-id="ea62b-107">Création d'un contrôle ActiveX</span><span class="sxs-lookup"><span data-stu-id="ea62b-107">Write an ActiveX Control</span></span>

<span data-ttu-id="ea62b-108">De même que les autres contrôles de InfoPath, les contrôles ActiveX doivent prendre en charge des interfaces COM existantes :</span><span class="sxs-lookup"><span data-stu-id="ea62b-108">As with other controls in InfoPath, ActiveX controls should support existing Component Object Model (COM) interfaces:</span></span>
  
- <span data-ttu-id="ea62b-109">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="ea62b-109">**IDispatch**</span></span>
    
- <span data-ttu-id="ea62b-110">**IPersistPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="ea62b-110">**IPersistPropertyBag**</span></span>
    
- <span data-ttu-id="ea62b-111">**IPersistStreamInit**</span><span class="sxs-lookup"><span data-stu-id="ea62b-111">**IPersistStreamInit**</span></span>
    
- <span data-ttu-id="ea62b-112">**IPropertyPage**</span><span class="sxs-lookup"><span data-stu-id="ea62b-112">**IPropertyPage**</span></span>
    
- <span data-ttu-id="ea62b-113">**IObjectSafety**</span><span class="sxs-lookup"><span data-stu-id="ea62b-113">**IObjectSafety**</span></span>
    
- <span data-ttu-id="ea62b-114">**IPropertyNotifySink**</span><span class="sxs-lookup"><span data-stu-id="ea62b-114">**IPropertyNotifySink**</span></span>
    
- <span data-ttu-id="ea62b-115">**IViewObject**</span><span class="sxs-lookup"><span data-stu-id="ea62b-115">**IViewObject**</span></span>
    
- <span data-ttu-id="ea62b-116">**IOleObject**</span><span class="sxs-lookup"><span data-stu-id="ea62b-116">**IOleObject**</span></span>
    
- <span data-ttu-id="ea62b-117">**IOleInPlaceObject**</span><span class="sxs-lookup"><span data-stu-id="ea62b-117">**IOleInPlaceObject**</span></span>
    
<span data-ttu-id="ea62b-118">Afin que InfoPath mette à jour des propriétés du modèle objet de document (DOM, Document Object Model) au moment où ils changent dans le contrôle, le contrôle doit implémenter les interfaces ci-après.</span><span class="sxs-lookup"><span data-stu-id="ea62b-118">In order for InfoPath to update properties in the Document Object Model (DOM) at the time that they change in the control, the control should implement the following interfaces:</span></span>
  
- <span data-ttu-id="ea62b-119">**IConnectionPointContainer**</span><span class="sxs-lookup"><span data-stu-id="ea62b-119">**IConnectionPointContainer**</span></span>
    
- <span data-ttu-id="ea62b-120">**IEnumConnectionPoints**</span><span class="sxs-lookup"><span data-stu-id="ea62b-120">**IEnumConnectionPoints**</span></span>
    
- <span data-ttu-id="ea62b-121">**IConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="ea62b-121">**IConnectionPoint**</span></span>
    
- <span data-ttu-id="ea62b-122">**IEnumConnections**</span><span class="sxs-lookup"><span data-stu-id="ea62b-122">**IEnumConnections**</span></span>
    
<span data-ttu-id="ea62b-123">De plus, il existe deux interfaces COM propres à InfoPath qui fournissent une meilleure intégration des contrôles :</span><span class="sxs-lookup"><span data-stu-id="ea62b-123">Also, there are two InfoPath-specific COM interfaces that provide tighter integration of controls:</span></span>
  
- [<span data-ttu-id="ea62b-124">IInfoPathControl</span><span class="sxs-lookup"><span data-stu-id="ea62b-124">IInfoPathControl</span></span>](https://msdn.microsoft.com/library/bb264625.aspx)
    
- [<span data-ttu-id="ea62b-125">IInfoPathControlSite</span><span class="sxs-lookup"><span data-stu-id="ea62b-125">IInfoPathControlSite</span></span>](https://msdn.microsoft.com/library/bb264627.aspx)
    
## <a name="add-an-activex-control-to-the-infopath-design-environment"></a><span data-ttu-id="ea62b-126">Ajout d'un contrôle ActiveX à l'environnement de création InfoPath </span><span class="sxs-lookup"><span data-stu-id="ea62b-126">Add an ActiveX Control to the InfoPath Design Environment</span></span>

<span data-ttu-id="ea62b-p103">La commande **Ajouter ou supprimer des contrôles personnalisés** dans le volet de tâches **Contrôles** vous permet d'utiliser l' **Assistant Ajout de contrôle personnalisé** pour ajouter un contrôle personnalisé. En utilisant l'assistant, vous pouvez sélectionner un contrôle ActiveX déjà enregistré ou rechercher des contrôles personnalisés supplémentaires sur Office Marketplace. Après avoir sélectionné un contrôle, vous pouvez spécifier les éléments ci-après.</span><span class="sxs-lookup"><span data-stu-id="ea62b-p103">The **Add or Remove Custom Controls** command on the **Controls** task pane enables you to use the **Add Custom Control Wizard** to add a custom control. By using the wizard, you can select an ActiveX control that has already been registered or find additional custom controls on Office Marketplace. After you select a control, you can specify the following items.</span></span> 
  
- <span data-ttu-id="ea62b-130">Spécifiez un CAB pour installer le contrôle ActiveX avec votre modèle de formulaire.</span><span class="sxs-lookup"><span data-stu-id="ea62b-130">Specify a CAB to install the ActiveX control with your form template.</span></span>
    
- <span data-ttu-id="ea62b-131">Spécifiez une propriété de liaison pour lier à XML.</span><span class="sxs-lookup"><span data-stu-id="ea62b-131">Specify a binding property to bind to the XML.</span></span>
    
- <span data-ttu-id="ea62b-132">Spécifiez une propriété utilisée pour activer ou désactiver le contrôle en fonction de règles ou de signatures numériques. Cela peut être utile, notamment, lorsque XML n'est pas présent ou qu'une mise en forme conditionnelle est utilisée.</span><span class="sxs-lookup"><span data-stu-id="ea62b-132">Specify a property that is used to enable or disable the control in response to rules or digital signatures, which can be useful, for example, when the XML is not present or when conditional formatting is used.</span></span>
    
- <span data-ttu-id="ea62b-133">Spécifiez la liaison du type de données.</span><span class="sxs-lookup"><span data-stu-id="ea62b-133">Specify data type binding.</span></span>
    
> [!NOTE]
> <span data-ttu-id="ea62b-134">[!REMARQUE] Si vous développez un contrôle ActiveX et l'ajoutez au volet de tâches **Contrôles** de InfoPath, vous ne pouvez pas le recréer tant que InfoPath n'est pas fermé.</span><span class="sxs-lookup"><span data-stu-id="ea62b-134">If you are developing an ActiveX control and have added it to the **Controls** task pane in InfoPath, you will be unable to rebuild the ActiveX control until InfoPath is closed.</span></span> 
  
## <a name="deploy-an-activex-control"></a><span data-ttu-id="ea62b-135">Déploiement d'un contrôle ActiveX</span><span class="sxs-lookup"><span data-stu-id="ea62b-135">Deploy an ActiveX Control</span></span>

<span data-ttu-id="ea62b-p104">Pour distribuer un contrôle ActiveX, vous pouvez écrire un programme d'installation qui installe le contrôle sur l'ordinateur cible et copie le fichier de modèle de contrôle (ICT) InfoPath et le fichier CAB dans le dossier de l'utilisateur, \Users\\<nom d'utilisateur\>\AppData\Local\Microsoft\InfoPath\Controls. Notez que si deux développeurs ou plus participent au développement de formulaires utilisant des contrôles ActiveX, chaque développeur doit disposer des contrôles ajoutés à l'environnement de création InfoPath, sinon il ne peut pas modifier les propriétés des contrôles de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="ea62b-p104">To distribute an ActiveX control, you can write an installer that installs the control on the target computer and copies the InfoPath Control Template (ICT) file and the CAB file to the user's folder, \Users\\<username\>\AppData\Local\Microsoft\InfoPath\Controls. Note that if two or more developers are collaborating on developing forms that use ActiveX controls, each developer should have the controls that were added to the InfoPath design environment, or they will be unable to modify the properties of the controls from InfoPath.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ea62b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea62b-138">See also</span></span>

<span data-ttu-id="ea62b-139">Labo 6 : Ajout de contrôles ActiveX à InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="ea62b-139">Lab 6: Adding ActiveX Controls in InfoPath 2003</span></span>
  
[<span data-ttu-id="ea62b-140">Création d'un contrôle InfoPath personnalisé à l'aide de C# et .NET (blog de l'équipe InfoPath) (éventuellement en anglais)</span><span class="sxs-lookup"><span data-stu-id="ea62b-140">Creating an InfoPath Custom Control using C# and .NET (InfoPath Team Blog)</span></span>](https://blogs.msdn.microsoft.com/infopath/2005/04/15/creating-an-infopath-custom-control-using-c-and-net/)

