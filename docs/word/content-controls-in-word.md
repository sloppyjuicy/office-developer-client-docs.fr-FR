---
title: Contrôles de contenu dans Word
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
keywords:
- Contrôles de contenu [Word], contrôles de contenu [Word], nouveautés
ms.assetid: c0e6dd3b-fae1-453d-a9b4-7f456b5172db
description: Découvrez les nouveaux scénarios de document structuré que permettent de déployer les contrôles de contenu Microsoft Word 2013.
localization_priority: Priority
ms.openlocfilehash: 4234425cc8398d87b72108d389953fc0eb802c87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358657"
---
# <a name="content-controls-in-word"></a><span data-ttu-id="c87f7-104">Contrôles de contenu dans Word</span><span class="sxs-lookup"><span data-stu-id="c87f7-104">Content controls in Word</span></span>

<span data-ttu-id="c87f7-105">Découvrez les nouveaux scénarios de document structuré que permettent de déployer les contrôles de contenu Microsoft Word 2013.</span><span class="sxs-lookup"><span data-stu-id="c87f7-105">Learn how Microsoft Word 2013 content controls enable a larger range of structured document scenarios.</span></span>

<span data-ttu-id="c87f7-106">Cette rubrique fournit des informations sur les modifications apportées aux contrôles de contenu dans Microsoft Word 2013 et sur les scénarios de document qui peuvent être déployés grâce à ces modifications.</span><span class="sxs-lookup"><span data-stu-id="c87f7-106">This topic provides information about changes to content controls in Microsoft Word 2013 and the document scenarios that those changes enable.</span></span>
  
### <a name="structured-documents"></a><span data-ttu-id="c87f7-107">Documents structurés</span><span class="sxs-lookup"><span data-stu-id="c87f7-107">Structured documents</span></span>
<span data-ttu-id="c87f7-108"><a name="WordCC_StructuredDocs"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-108"></span></span>

<span data-ttu-id="c87f7-109">Les documents structurés sont des documents qui contrôlent où le contenu peut s’afficher dans un document, quel type de contenu peut s’afficher dans le document et si ce contenu peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="c87f7-109">Structured documents are documents that control where content can appear on a document, what kind of content can appear in the document, and whether that content can be edited.</span></span>
  
<span data-ttu-id="c87f7-110">Voici quelques scénarios courants pour un contenu structuré dans Microsoft Word :</span><span class="sxs-lookup"><span data-stu-id="c87f7-110">Here are some common scenarios for structured content in Microsoft Word:</span></span>
  
- <span data-ttu-id="c87f7-111">Un cabinet d’avocats a besoin de créer des documents qui contiennent des passages juridiques qui ne doivent pas être modifiés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c87f7-111">A legal firm needs to create documents that contain legal language that should not be changed by the user.</span></span>
    
- <span data-ttu-id="c87f7-112">Une entreprise a besoin de créer une page de garde pour les propositions où seuls le titre, l’auteur et la date sont saisis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c87f7-112">A business needs to create a proposal cover page where only the title, author, and date are entered by the user.</span></span>
    
- <span data-ttu-id="c87f7-113">Une entreprise a besoin de créer des factures dans lesquelles les données du client sont incluses dans des zones prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="c87f7-113">A business needs to create invoices where the customer data is included in the invoice at predefined regions.</span></span>
    
### <a name="using-content-controls-to-structure-a-document"></a><span data-ttu-id="c87f7-114">Utilisation des contrôles de contenu pour structurer un document</span><span class="sxs-lookup"><span data-stu-id="c87f7-114">Using content controls to structure a document</span></span>
<span data-ttu-id="c87f7-115"><a name="WordCC_StructuredDocs"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-115"></span></span>

<span data-ttu-id="c87f7-116">Les contrôles de contenu sont des entités Microsoft Word qui agissent comme des conteneurs pour un contenu spécifique dans un document.</span><span class="sxs-lookup"><span data-stu-id="c87f7-116">Content controls are Microsoft Word entities that act as containers for specific content in a document.</span></span> <span data-ttu-id="c87f7-117">Chaque contrôle de contenu peut comporter des dates, des listes ou des paragraphes de texte mis en forme.</span><span class="sxs-lookup"><span data-stu-id="c87f7-117">Individual content controls can contain content such as dates, lists, or paragraphs of formatted text.</span></span> <span data-ttu-id="c87f7-118">Les contrôles de contenu vous aident à créer des blocs de contenu enrichi, structuré, et sont conçus pour être utilisés dans les modèles qui insèrent des blocs bien définis dans vos documents, créant ainsi des documents structurés.</span><span class="sxs-lookup"><span data-stu-id="c87f7-118">Content controls help you to create rich, structured blocks of content and are designed for use in templates that insert well-defined blocks into your documents, creating structured documents.</span></span>
  
<span data-ttu-id="c87f7-119">Les contrôles de contenu sont idéaux pour la création de documents structurés, car ils vous permettent d’ajuster la position du contenu, de spécifier le type de contenu (par exemple, une date, une image ou du texte), de limiter ou d’activer la modification et d’ajouter une sémantique au contenu.</span><span class="sxs-lookup"><span data-stu-id="c87f7-119">Content controls are ideal for creating structured documents because content controls help you fix the position of content, specify the kind of content (for example, a date, a picture, or text), restrict or enable editing, and add semantic meaning to content.</span></span>
  
### <a name="content-controls-in-word-2010"></a><span data-ttu-id="c87f7-120">Contrôles de contenu dans Word 2010</span><span class="sxs-lookup"><span data-stu-id="c87f7-120">Content controls in Word 2010</span></span>
<span data-ttu-id="c87f7-121"><a name="WordCC_StructuredDocs"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-121"></span></span>

<span data-ttu-id="c87f7-122">Les contrôles de contenu suivants sont disponibles dans Word 2010 :</span><span class="sxs-lookup"><span data-stu-id="c87f7-122">The following content controls are available in Word 2010:</span></span>
  
- <span data-ttu-id="c87f7-123">Texte enrichi</span><span class="sxs-lookup"><span data-stu-id="c87f7-123">Rich Text</span></span>
    
- <span data-ttu-id="c87f7-124">Texte brut</span><span class="sxs-lookup"><span data-stu-id="c87f7-124">Plain Text</span></span>
    
- <span data-ttu-id="c87f7-125">Image</span><span class="sxs-lookup"><span data-stu-id="c87f7-125">Picture</span></span>
    
- <span data-ttu-id="c87f7-126">Galerie de blocs de construction</span><span class="sxs-lookup"><span data-stu-id="c87f7-126">Building Block Gallery</span></span>
    
- <span data-ttu-id="c87f7-127">Zone de liste modifiable</span><span class="sxs-lookup"><span data-stu-id="c87f7-127">Combo Box</span></span>
    
- <span data-ttu-id="c87f7-128">Liste déroulante</span><span class="sxs-lookup"><span data-stu-id="c87f7-128">Drop-Down List</span></span>
    
- <span data-ttu-id="c87f7-129">Date</span><span class="sxs-lookup"><span data-stu-id="c87f7-129">Date</span></span>
    
- <span data-ttu-id="c87f7-130">Case à cocher</span><span class="sxs-lookup"><span data-stu-id="c87f7-130">Checkbox</span></span>
    
- <span data-ttu-id="c87f7-131">Groupe</span><span class="sxs-lookup"><span data-stu-id="c87f7-131">Group</span></span>
    
<span data-ttu-id="c87f7-132">Les contrôles de contenu Word 2010 permettent d’obtenir diverses solutions de document structuré potentielles. Toutefois, dans Word 2013, les contrôles de contenu permettent de déployer encore davantage de scénarios.</span><span class="sxs-lookup"><span data-stu-id="c87f7-132">Word 2010 content controls enable various potential structured document solutions, but in Word 2013 content controls enable a greater range of scenarios.</span></span>
  
## <a name="content-control-improvements-in-word-2013"></a><span data-ttu-id="c87f7-133">Améliorations des contrôles de contenu dans Word 2013</span><span class="sxs-lookup"><span data-stu-id="c87f7-133">Content control improvements in Word 2013</span></span>
<span data-ttu-id="c87f7-134"><a name="WordCC_WhatsNew"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-134"></span></span>

<span data-ttu-id="c87f7-135">Dans Word 2013, trois améliorations principales ont été apportées aux contrôles de contenu : une meilleure visualisation, la prise en charge du mappage XML pour les contrôles de contenu de texte enrichi et un nouveau contrôle de contenu pour le contenu qui se répète.</span><span class="sxs-lookup"><span data-stu-id="c87f7-135">In Word 2013, content controls provide three key improvements: improved visualization, support for XML Mapping for Rich Text content controls, and a new content control for repeating content.</span></span>
  
### <a name="improved-visualization"></a><span data-ttu-id="c87f7-136">Meilleure visualisation</span><span class="sxs-lookup"><span data-stu-id="c87f7-136">Improved visualization</span></span>

<span data-ttu-id="c87f7-137">Word 2013 permet aux contrôles de contenu individuels de s’afficher de trois façons possibles :</span><span class="sxs-lookup"><span data-stu-id="c87f7-137">Word 2013 allows an individual content control to appear in one of three possible states:</span></span>
  
- <span data-ttu-id="c87f7-138">Cadre englobant</span><span class="sxs-lookup"><span data-stu-id="c87f7-138">Bounding box</span></span>
    
- <span data-ttu-id="c87f7-139">Balises de début et de fin</span><span class="sxs-lookup"><span data-stu-id="c87f7-139">Start/End tags</span></span>
    
- <span data-ttu-id="c87f7-140">Aucun</span><span class="sxs-lookup"><span data-stu-id="c87f7-140">None</span></span>
    
> [!NOTE]
> <span data-ttu-id="c87f7-141">Sauf mention contraire, cette section traite de la visualisation des contrôles de contenu lorsque le document n’est pas affiché en **mode Création**. Pour définir le mode d’affichage d’un contrôle de contenu, utilisez la liste déroulante **Afficher en tant que** dans la boîte de dialogue **Propriétés du contrôle de contenu**.</span><span class="sxs-lookup"><span data-stu-id="c87f7-141">If not stated otherwise, this section discusses the visualization of content controls when the document is not viewed in **Design Mode**.You set the display mode for a content control by using the **Show as** drop-down list control in the **Content Control Properties** dialog box.</span></span> 
  
<span data-ttu-id="c87f7-142">**Figure 1. Boîte de dialogue Propriétés du contrôle de contenu**</span><span class="sxs-lookup"><span data-stu-id="c87f7-142">**Figure 1. Content Control Properties dialog box**</span></span>

<span data-ttu-id="c87f7-143">![Boîte de dialogue Propriétés du contrôle de contenu](media/DK2_WordCC_Fig01.jpg "Boîte de dialogue Propriétés du contrôle de contenu")</span><span class="sxs-lookup"><span data-stu-id="c87f7-143">![Content control properties dialog box](media/DK2_WordCC_Fig01.jpg "Content control properties dialog box")</span></span>
  
<span data-ttu-id="c87f7-144">Vous pouvez également définir le mode d’affichage d’un contrôle de contenu à l’aide du modèle objet Word 2013 (décrit plus loin dans [Nouveaux membres de modèle objet client de contrôle de contenu Word 2013](#WordCC_NewOM)).</span><span class="sxs-lookup"><span data-stu-id="c87f7-144">You can also set the display mode for a content control by using the Word 2013 object model (discussed later in [New Word 2013 content control object model members](#WordCC_NewOM)).</span></span>
  
### <a name="bounding-box"></a><span data-ttu-id="c87f7-145">Cadre englobant</span><span class="sxs-lookup"><span data-stu-id="c87f7-145">Bounding box</span></span>
<span data-ttu-id="c87f7-146"><a name="WordCC_DefaultRendering"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-146"></span></span>

<span data-ttu-id="c87f7-147">Le rendu par défaut pour les contrôles de contenu dans Word 2013 est de préserver l’apparence des contrôles de contenu tels qu’ils apparaissent dans Word 2007 et Word 2010 ; autrement dit, comme cadre englobant.</span><span class="sxs-lookup"><span data-stu-id="c87f7-147">The default rendering for content controls in Word 2013 is to preserve the look of content controls as they appear in Word 2007 and Word 2010; that is, as a bounding box.</span></span> <span data-ttu-id="c87f7-148">Lorsqu’un contrôle de contenu est défini pour apparaître comme **cadre englobant**, l’affichage change en fonction de l’interaction utilisateur suivante :</span><span class="sxs-lookup"><span data-stu-id="c87f7-148">When a content control is set to show as **Bounding Box**, the display changes depending upon the following user interaction:</span></span>
  
- <span data-ttu-id="c87f7-149">Lorsque le contrôle de contenu n’est pas activé, aucune visualisation ne se produit</span><span class="sxs-lookup"><span data-stu-id="c87f7-149">When the content control does not have the focus, no visualization occurs</span></span>
    
- <span data-ttu-id="c87f7-150">Lorsque vous pointez dessus avec la souris, le contrôle de contenu apparaît sous la forme d’un rectangle ombré</span><span class="sxs-lookup"><span data-stu-id="c87f7-150">On mouse-over, the content control appears as a shaded rectangle</span></span>
    
<span data-ttu-id="c87f7-151">**Figure 2. Contrôle de contenu lors du pointage avec la souris**</span><span class="sxs-lookup"><span data-stu-id="c87f7-151">**Figure 2. Content control on mouse-over**</span></span>

<span data-ttu-id="c87f7-152">![Contrôle de contenu lors du pointage avec la souris](media/DK2_WordCC_Fig02.jpg "Contrôle de contenu lors du pointage avec la souris")</span><span class="sxs-lookup"><span data-stu-id="c87f7-152">![Content control on mouse over](media/DK2_WordCC_Fig02.jpg "Content control on mouse over")</span></span>
  
- <span data-ttu-id="c87f7-153">Lorsque le contrôle de contenu est activé (c’est-à-dire lorsque l’utilisateur clique sur le contrôle de contenu), il s’affiche comme un « cadre englobant » (avec une ligne autour du contenu et le titre, si un titre a été défini)</span><span class="sxs-lookup"><span data-stu-id="c87f7-153">When the content control has the focus (when the user chooses the content control), the control appears as a "bounding box" (with a line around the content and the title showing, if a title has been set)</span></span>
    
<span data-ttu-id="c87f7-154">**Figure 3. Contrôle de contenu activé**</span><span class="sxs-lookup"><span data-stu-id="c87f7-154">**Figure 3. Content control with focus**</span></span>

<span data-ttu-id="c87f7-155">![Contrôle de contenu activé](media/DK2_WordCC_Fig03.jpg "Contrôle de contenu activé")</span><span class="sxs-lookup"><span data-stu-id="c87f7-155">![Content control with focus](media/DK2_WordCC_Fig03.jpg "Content control with focus")</span></span>
  
### <a name="startend-tags"></a><span data-ttu-id="c87f7-156">Balises de début et de fin</span><span class="sxs-lookup"><span data-stu-id="c87f7-156">Start/End tags</span></span>
<span data-ttu-id="c87f7-157"><a name="WordCC_StartEndTags"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-157"></span></span>

<span data-ttu-id="c87f7-158">Lorsque le contrôle de contenu est configuré pour s’afficher entre des **balises de début et de fin**, les balises s’affichent, qu’il y ait une interaction de l’utilisateur ou non, et le titre ne s’affiche jamais ; mais les boutons, tels que le bouton **Liste déroulante**, apparaissent lorsque vous pointez dessus avec la souris.</span><span class="sxs-lookup"><span data-stu-id="c87f7-158">When the content control is set to show as **Start/End tag**, the tags are displayed regardless of user interaction, and the title never appears; but buttons, such as the **Drop-Down List** button, appear on mouse over.</span></span> 
  
<span data-ttu-id="c87f7-159">**Figure 4. Contrôle de contenu défini pour s’afficher entre des balises de début et de fin**</span><span class="sxs-lookup"><span data-stu-id="c87f7-159">**Figure 4. Content control set to show as start/end tags**</span></span>

<span data-ttu-id="c87f7-160">![Contrôle de contenu défini pour s’afficher entre des balises de début et de fin](media/DK2_WordCC_Fig04.jpg "Contrôle de contenu défini pour s’afficher entre des balises de début et de fin")</span><span class="sxs-lookup"><span data-stu-id="c87f7-160">![Content control set to show as start and end tags](media/DK2_WordCC_Fig04.jpg "Content control set to show as start and end tags")</span></span>
  
### <a name="none"></a><span data-ttu-id="c87f7-161">Aucun</span><span class="sxs-lookup"><span data-stu-id="c87f7-161">None</span></span>
<span data-ttu-id="c87f7-162"><a name="WordCC_Invisible"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-162"></span></span>

<span data-ttu-id="c87f7-163">Lorsque l’affichage du contrôle de contenu est défini sur **Aucun**, le contrôle de contenu n’est pas affiché.</span><span class="sxs-lookup"><span data-stu-id="c87f7-163">When the content control is set to show as **None**, the content control is not displayed.</span></span>
  
### <a name="content-control-colorization"></a><span data-ttu-id="c87f7-164">Colorisation des contrôles de contenu</span><span class="sxs-lookup"><span data-stu-id="c87f7-164">Content control colorization</span></span>
<span data-ttu-id="c87f7-165"><a name="WordCC_CCColorization"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-165"></span></span>

<span data-ttu-id="c87f7-166">Outre l’activation d’un autre type d’affichage pour un contrôle de contenu, Word 2013 vous aide également à définir la couleur pour un contrôle de contenu individuel.</span><span class="sxs-lookup"><span data-stu-id="c87f7-166">In addition to enabling a different kind of display for a content control, Word 2013 also helps you to set the color for an individual content control.</span></span> <span data-ttu-id="c87f7-167">Vous définissez la couleur d’un contrôle de contenu à l’aide du bouton **Couleur**dans la boîte de dialogue **Propriétés du contrôle de contenu**.</span><span class="sxs-lookup"><span data-stu-id="c87f7-167">You set the color of a content control by using the **Color** button in the **Content Control Properties** dialog box.</span></span> 
  
<span data-ttu-id="c87f7-168">Vous pouvez également définir la couleur d’un contrôle de contenu à l’aide du modèle objet Word 2013 (décrit plus loin dans [Nouveaux membres de modèle objet client de contrôle de contenu Word 2013](#WordCC_NewOM)).</span><span class="sxs-lookup"><span data-stu-id="c87f7-168">You can also set the color of a content control by using the Word 2013 object model (discussed later in [New Word 2013 content control object model members](#WordCC_NewOM)).</span></span>
  
<span data-ttu-id="c87f7-169">**Figure 5. Boîte de dialogue Propriétés du contrôle de contenu**</span><span class="sxs-lookup"><span data-stu-id="c87f7-169">**Figure 5. Content Control Properties dialog box**</span></span>

<span data-ttu-id="c87f7-170">![Boîte de dialogue Propriétés du contrôle de contenu](media/DK2_WordCC_Fig05.jpg "Boîte de dialogue Propriétés du contrôle de contenu")</span><span class="sxs-lookup"><span data-stu-id="c87f7-170">![Content control properties dialog box](media/DK2_WordCC_Fig05.jpg "Content control properties dialog box")</span></span>
  
### <a name="support-for-xml-mapping-for-rich-text-content-controls"></a><span data-ttu-id="c87f7-171">Prise en charge du mappage XML pour les contrôles de contenu de texte enrichi</span><span class="sxs-lookup"><span data-stu-id="c87f7-171">Support for XML mapping for rich text content controls</span></span>
<span data-ttu-id="c87f7-172"><a name="WordCC_XMLMapping"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-172"></span></span>

<span data-ttu-id="c87f7-173">Word 2013 vous permet de mapper le contenu des contrôles de contenu de texte enrichi et les contrôles de contenu de bloc de construction de document sur le magasin de données XML.</span><span class="sxs-lookup"><span data-stu-id="c87f7-173">Word 2013 helps you to map the content of rich text content controls and document building block content controls to the XML data store.</span></span> <span data-ttu-id="c87f7-174">Pour ce faire, vous définissez le *mappage XML* pour le contrôle de contenu.</span><span class="sxs-lookup"><span data-stu-id="c87f7-174">To do this, you set the  *XML mapping*  for the content control.</span></span> <span data-ttu-id="c87f7-175">Vous pouvez définir cette propriété à l’aide de la méthode **XMLMapping.SetMapping** existante dans le modèle objet.</span><span class="sxs-lookup"><span data-stu-id="c87f7-175">You can set this property by using the existing **XMLMapping.SetMapping** method in the object model.</span></span> <span data-ttu-id="c87f7-176">Dans la partie XML personnalisée, le XML personnalisé est stocké comme balisage plat Open XML converti en chaîne (en utilisant le codage XML standard), pour pouvoir être stocké comme nœud de texte dans la partie XML personnalisée.</span><span class="sxs-lookup"><span data-stu-id="c87f7-176">Within the custom XML part, the custom XML is stored as flat Open XML markup converted into a string (by using standard XML encoding), so that it can be stored as a text node in the custom XML part.</span></span> <span data-ttu-id="c87f7-177">Toutefois, le mappage a toujours la même limite : il peut mapper uniquement sur des nœuds terminaux ou des attributs feuilles.</span><span class="sxs-lookup"><span data-stu-id="c87f7-177">However, the mapping continues to have the limitation that it can only successfully map to leaf nodes or attributes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c87f7-p105">Les contrôles de contenu de texte enrichi ne peuvent pas contenir d’autres contrôles de contenu de texte enrichi. S’il en existe un au sein d’un autre (par exemple, suite à une manipulation du format de fichier, d’une opération de copier/coller, etc.), il n’est pas lié tant qu’il est contenu dans un contrôle de texte enrichi mappé.</span><span class="sxs-lookup"><span data-stu-id="c87f7-p105">Rich text content controls cannot contain other rich text content controls. If one exists inside of another (for example, because of file format manipulation, copy and paste, and so on), it is unlinked until it is no longer contained inside a mapped rich text control.</span></span> 
  
<span data-ttu-id="c87f7-180">Pour plus d’informations sur la configuration d’un mappage XML, consultez la section [Nouveaux membres de modèle objet client de contrôle de contenu Word 2013](#WordCC_NewOM) plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="c87f7-180">For more information about how to set up XML mapping, see the section [New Word 2013 content control object model members](#WordCC_NewOM) later in this topic.</span></span> 
  
### <a name="supporting-repeating-content"></a><span data-ttu-id="c87f7-181">Prise en charge du contenu répétitif</span><span class="sxs-lookup"><span data-stu-id="c87f7-181">Supporting repeating content</span></span>
<span data-ttu-id="c87f7-182"><a name="WordCC_SupportingRepeating"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-182"></span></span>

<span data-ttu-id="c87f7-183">Outre les améliorations de la visualisation et la prise en charge pour le mappage XML sur des contrôles de contenu de texte enrichi, Word 2013 ajoute également un nouveau contrôle de contenu qui vous permet de répéter le contenu.</span><span class="sxs-lookup"><span data-stu-id="c87f7-183">In addition to visualization enhancements and support for XML mapping to rich text content controls, Word 2013 also adds a new content control that enables you to repeat content.</span></span> <span data-ttu-id="c87f7-184">Le contrôle de contenu répétitif répète le contenu qu’il contient, ainsi que d’autres contrôles de contenu.</span><span class="sxs-lookup"><span data-stu-id="c87f7-184">The repeating section content control repeats the content contained within it, including other content controls.</span></span>
  
<span data-ttu-id="c87f7-p107">Vous insérez le contrôle de contenu répétitif autour de paragraphes entiers ou de lignes de table. Une fois que le contrôle entoure une section, vous pouvez insérer des copies de la section au-dessus ou en dessous de la section contenue.</span><span class="sxs-lookup"><span data-stu-id="c87f7-p107">You insert the repeating section content control around entire paragraphs or table rows. Once the control surrounds a section, you can insert copies of the section above or below the contained section.</span></span>
  
<span data-ttu-id="c87f7-187">**Figure 6. Menu contextuel de contrôle de contenu répétitif**</span><span class="sxs-lookup"><span data-stu-id="c87f7-187">**Figure 6. Repeating section content control context menu**</span></span>

<span data-ttu-id="c87f7-188">![Menu contextuel de contrôle de contenu répétitif](media/DK2_WordCC_Fig06.jpg "Menu contextuel de contrôle de contenu répétitif")</span><span class="sxs-lookup"><span data-stu-id="c87f7-188">![Repeating section content control context](media/DK2_WordCC_Fig06.jpg "Repeating section content control context")</span></span>
  
<span data-ttu-id="c87f7-189">Vous pouvez répéter la section insérée en utilisant le contrôle sur la fin du contrôle de contenu (affiché sous la forme d’un bouton avec un signe plus (![Signe plus](media/DK2_WordCC_Fig06A.jpg "Signe plus"))) ou en choisissant une commande dans le menu contextuel, comme illustré dans la Figure 6.</span><span class="sxs-lookup"><span data-stu-id="c87f7-189">You can repeat the inserted section by using either the control on the end of the content control (displayed as a button with a plus sign (![Plus sign](media/DK2_WordCC_Fig06A.jpg "Plus sign"))) or by choosing a command on the context menu, as shown in Figure 6.</span></span> <span data-ttu-id="c87f7-190">Le contenu répété devient une section distincte du contrôle à laquelle vous pouvez attribuer un titre à l’aide de la boîte de dialogue **Propriétés du contrôle de contenu**.</span><span class="sxs-lookup"><span data-stu-id="c87f7-190">The repeated content becomes a separate section of the control that you can assign a title by using the **Content Control Properties** dialog box.</span></span> 
  
<span data-ttu-id="c87f7-191">**Figure 7. Attribution d’un titre de section dans la boîte de dialogue Propriétés du contrôle de contenu**</span><span class="sxs-lookup"><span data-stu-id="c87f7-191">**Figure 7. Assign a section title in the Content Control Properties dialog box**</span></span>

<span data-ttu-id="c87f7-192">![Boîte de dialogue Propriétés du contrôle de contenu](media/DK2_WordCC_Fig07.jpg "Boîte de dialogue Propriétés du contrôle de contenu")</span><span class="sxs-lookup"><span data-stu-id="c87f7-192">![Content control properties dialog box](media/DK2_WordCC_Fig07.jpg "Content control properties dialog box")</span></span>
  
<span data-ttu-id="c87f7-193">Une fois que vous avez donné un titre à la section, si vous sélectionnez **Autoriser les utilisateurs à ajouter et à supprimer des sections** dans la boîte de dialogue **Propriétés du contrôle de contenu**, les utilisateurs peuvent ajouter ou supprimer la section par nom.</span><span class="sxs-lookup"><span data-stu-id="c87f7-193">Once you have given the section a title, if you select **Allow users to add and remove sections** in the **Content Control Properties** dialog box, users can add or delete the section by name.</span></span> 
  
<span data-ttu-id="c87f7-194">**Figure 8. Utilisation du menu contextuel de contrôle de contenu répétitif pour supprimer une section**</span><span class="sxs-lookup"><span data-stu-id="c87f7-194">**Figure 8. Use the repeating section content control context menu to delete a section**</span></span>

<span data-ttu-id="c87f7-195">![Menu contextuel de contrôle de contenu répétitif](media/DK2_WordCC_Fig08.jpg "Menu contextuel de contrôle de contenu répétitif")</span><span class="sxs-lookup"><span data-stu-id="c87f7-195">![Repeating section content control context](media/DK2_WordCC_Fig08.jpg "Repeating section content control context")</span></span>
  
<span data-ttu-id="c87f7-p109">Lorsqu’un contrôle de contenu répétitif entoure d’autres contrôles de contenu, les contrôles de contenu entourés sont répétés dans chaque nouvel élément ; mais le contenu de tous ces contrôles de contenu est rétabli sur le texte d’espace réservé. Il existe deux exceptions pour lesquelles le contenu des contrôles enfants est conservé :</span><span class="sxs-lookup"><span data-stu-id="c87f7-p109">When a repeating section content control surrounds other content controls, the enclosed content controls are repeated in each new item; but any such content controls have their contents reset to placeholder text. There are two exceptions where child control contents are preserved:</span></span> 
  
- <span data-ttu-id="c87f7-198">Lorsqu’un contrôle enfant est un contrôle répétitif.</span><span class="sxs-lookup"><span data-stu-id="c87f7-198">When a child control is a repeating section control.</span></span>
    
- <span data-ttu-id="c87f7-199">Lorsqu’un contrôle enfant présente un mappage XML à un nœud à l’extérieur du contrôle de contenu répétitif.</span><span class="sxs-lookup"><span data-stu-id="c87f7-199">When a child control is XML-mapped to a node outside the repeating section content control.</span></span>
    
<span data-ttu-id="c87f7-200">**Figure 9. Contrôle de contenu répétitif contenant des contrôles enfants avant la répétition**</span><span class="sxs-lookup"><span data-stu-id="c87f7-200">**Figure 9. Repeating section content control containing child controls before repeat**</span></span>

<span data-ttu-id="c87f7-201">![Contrôle de contenu répétitif avant la répétition](media/DK2_WordCC_Fig09.jpg "Contrôle de contenu répétitif avant la répétition")</span><span class="sxs-lookup"><span data-stu-id="c87f7-201">![Repeating section content control before repeat](media/DK2_WordCC_Fig09.jpg "Repeating section content control before repeat")</span></span>
  
<span data-ttu-id="c87f7-202">**Figure 10. Contrôle de contenu répétitif contenant des contrôles enfants après la répétition**</span><span class="sxs-lookup"><span data-stu-id="c87f7-202">**Figure 10. Repeating section content control containing child controls after repeat**</span></span>

<span data-ttu-id="c87f7-203">![Contrôle de contenu répétitif après la répétition](media/DK2_WordCC_Fig10.jpg "Contrôle de contenu répétitif après la répétition")</span><span class="sxs-lookup"><span data-stu-id="c87f7-203">![Repeating section content control after repeat](media/DK2_WordCC_Fig10.jpg "Repeating section content control after repeat")</span></span>
  
### <a name="repeating-section-content-controls-around-xml-mapped-controls"></a><span data-ttu-id="c87f7-204">Contrôles de contenu répétitif autour de contrôles présentant un mappage XML</span><span class="sxs-lookup"><span data-stu-id="c87f7-204">Repeating section content controls around XML-mapped controls</span></span>
<span data-ttu-id="c87f7-205"><a name="WordCC_RepeatingSectionCCs"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-205"></span></span>

<span data-ttu-id="c87f7-206">Pour les mappages XML qui sont contenus dans une section répétitive, Word 2013 les mappe comme suit.</span><span class="sxs-lookup"><span data-stu-id="c87f7-206">For XML mappings that are contained in a repeating section, Word 2013 maps them as follows.</span></span>
  
<span data-ttu-id="c87f7-207">Si le mappage ne présente pas de référence croisée avec un élément du jeu de nœuds dans sa chaîne parent, la liaison est une « liaison absolue » et présente le même contenu dans tous les éléments de section répétitive.</span><span class="sxs-lookup"><span data-stu-id="c87f7-207">If the mapping does not intersect with an item in the node set as part of its parent chain, the binding is an "absolute binding" and shows the same content in all repeating section items.</span></span>
  
<span data-ttu-id="c87f7-208">Si le mappage présente une référence croisée à un élément du jeu de nœuds dans sa chaîne parent, la liaison est une « liaison relative » et est remappée comme suit :</span><span class="sxs-lookup"><span data-stu-id="c87f7-208">If the mapping does intersect with an item in the node set as part of its parent chain, the binding is a "relative binding", and is remapped as follows:</span></span>
  
- <span data-ttu-id="c87f7-209">La liaison absolue pour le nœud est déterminée (aplanissement des expressions de requête) ; cela doit se produire sur le mappage initial</span><span class="sxs-lookup"><span data-stu-id="c87f7-209">The absolute binding for the node is determined (flattening out any query expressions)─this should happen on initial mapping</span></span>
    
- <span data-ttu-id="c87f7-210">L’axe de la liaison qui présente une référence croisée avec le jeu de nœuds est supprimé.</span><span class="sxs-lookup"><span data-stu-id="c87f7-210">The axis of the binding that intersects with the node set is removed</span></span>
    
- <span data-ttu-id="c87f7-211">Le reste de l’expression XPath est évalué par rapport à l’expression XPath de l’élément de contenu répétitif</span><span class="sxs-lookup"><span data-stu-id="c87f7-211">The remainder of the XPath is evaluated relative to the XPath of the repeating section content item</span></span>
    
<span data-ttu-id="c87f7-212">Par exemple, les mappages suivants peuvent se produire :</span><span class="sxs-lookup"><span data-stu-id="c87f7-212">For example, the following mappings might occur:</span></span>
  
- <span data-ttu-id="c87f7-213">La section répétitive est mappée à \root\next\path</span><span class="sxs-lookup"><span data-stu-id="c87f7-213">The repeating section is mapped to \root\next\path</span></span>
    
- <span data-ttu-id="c87f7-214">Le contrôle dans l’exemple d’élément est mappé à \root\next\path[2]\baz</span><span class="sxs-lookup"><span data-stu-id="c87f7-214">The control in the sample item is mapped to \root\next\path[2]\baz</span></span>
    
- <span data-ttu-id="c87f7-215">Word met en correspondance \root\next\path[2] avec un élément dans le jeu de nœuds</span><span class="sxs-lookup"><span data-stu-id="c87f7-215">Word matches \root\next\path[2] to an item in the node set</span></span>
    
<span data-ttu-id="c87f7-216">La liaison est donc évaluée comme .\baz, où la base est le nœud de l’élément de contenu répétitif.</span><span class="sxs-lookup"><span data-stu-id="c87f7-216">The binding is therefore evaluated as .\baz, where the base is the node of the repeating content item.</span></span>
  
<span data-ttu-id="c87f7-217">Les suggestions suivantes pour utiliser des contrôles de contenu répétitif peuvent vous aider à éviter de perdre des données et d’être frustré.</span><span class="sxs-lookup"><span data-stu-id="c87f7-217">The following suggestions for working with repeating content controls can help you prevent data loss and avoid frustration.</span></span>
  
### <a name="working-with-repeating-section-content-controls-that-are-mapped-to-xml-data"></a><span data-ttu-id="c87f7-218">Utilisation des contrôles de contenu répétitif mappés à des données XML</span><span class="sxs-lookup"><span data-stu-id="c87f7-218">Working with repeating section content controls that are mapped to XML data</span></span>
<span data-ttu-id="c87f7-219"><a name="WordCC_RepeatingSectionCCs"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-219"></span></span>

<span data-ttu-id="c87f7-220">Si vous insérez un contrôle de contenu répétitif qui est mappé à des données XML, chaque fois que votre utilisateur ouvre de nouveau le document, Word recrée les éléments de la section répétitive, en fonction des informations du magasin de données.</span><span class="sxs-lookup"><span data-stu-id="c87f7-220">If you insert a repeating section content control that is mapped to XML data, every time your user reopens the document, Word recreates the repeating section items, based on the information in the data store.</span></span> <span data-ttu-id="c87f7-221">Même si vous enregistrez le document, les modifications que l’utilisateur apporte aux éléments de la section répétitive dans le document qui ne sont pas mappées également dans le magasin de données sont perdues.</span><span class="sxs-lookup"><span data-stu-id="c87f7-221">Even if you save the document, any changes that the user makes in the repeating section items in the document that aren't also mapped into the data store are lost.</span></span>
  
<span data-ttu-id="c87f7-222">Pour éviter que cela ne se produise, verrouillez le contrôle de contenu répétitif et n’autorisez l’utilisateur à apporter des modifications qu’aux contrôles de contenu enfants déverrouillés qui sont également mappés aux données XML.</span><span class="sxs-lookup"><span data-stu-id="c87f7-222">To help prevent this from happening, lock the repeating section content control and allow the user to edit only in unlocked child content controls that are mapped to the XML as well.</span></span>
  
### <a name="binding-a-repeating-section-content-control-to-a-table"></a><span data-ttu-id="c87f7-223">Liaison d’un contrôle de contenu répétitif à une table</span><span class="sxs-lookup"><span data-stu-id="c87f7-223">Binding a repeating section content control to a table</span></span>
<span data-ttu-id="c87f7-224"><a name="WordCC_RepeatingSectionCCs"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-224"></span></span>

<span data-ttu-id="c87f7-225">Si vous souhaitez lier un contrôle de contenu répétitif à une table, insérez la table *puis* insérez le contrôle de contenu répétitif, et non l’inverse </span><span class="sxs-lookup"><span data-stu-id="c87f7-225">If you want to bind a repeating section content control to a table, insert the table and  *then*  the insert repeating section content control, and not the other way around.</span></span> <span data-ttu-id="c87f7-226">(sinon, vous ne pourrez pas sélectionner uniquement la table).</span><span class="sxs-lookup"><span data-stu-id="c87f7-226">(Otherwise, you won't be able to select only the table).</span></span> 
  
### <a name="nesting-repeating-section-content-controls-within-a-table"></a><span data-ttu-id="c87f7-227">Imbrication de contrôles de contenu répétitif dans un tableau</span><span class="sxs-lookup"><span data-stu-id="c87f7-227">Nesting repeating section content controls within a table</span></span>
<span data-ttu-id="c87f7-228"><a name="WordCC_RepeatingSectionCCs"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-228"></span></span>

<span data-ttu-id="c87f7-229">L’imbrication étroite de contrôles de contenu répétitif au sein d’une table (par exemple, lorsque la fin du contrôle de contenu répétitif parent et la fin du contrôle de contenu répétitif enfant se trouvent dans la même cellule) entraîne la suppression de la section répétitive extérieure en cas de suppression ou d’ajout d’un élément dans la section intérieure.</span><span class="sxs-lookup"><span data-stu-id="c87f7-229">Nesting repeating section content controls tightly within a table (for example, when the end of the parent and child repeating section content control is in the same cell) causes the outer repeating section to be deleted when the inner section has an item added or removed.</span></span>
  
<span data-ttu-id="c87f7-p112">Pour éviter que cela ne se produise, ajoutez une marque de paragraphe entre la fin d’un contrôle de contenu répétitif et la fin du contrôle de contenu répétitif suivant. Pour masquer la marque de paragraphe, désactivez l’option **Afficher/Masquer** dans l’onglet **Accueil** du ruban.</span><span class="sxs-lookup"><span data-stu-id="c87f7-p112">You can prevent this from happening by adding a paragraph marker between the end of one repeating section content control and the next. To hide the paragraph marker, deselect the **Show/Hide** option on the **Home** tab of the ribbon.</span></span> 
  
### <a name="open-xml-file-format-schema-additions"></a><span data-ttu-id="c87f7-232">Ajouts au schéma au format Open XML</span><span class="sxs-lookup"><span data-stu-id="c87f7-232">Open XML File Format schema additions</span></span>
<span data-ttu-id="c87f7-233"><a name="WordCC"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-233"></span></span>

<span data-ttu-id="c87f7-234">Les éléments suivants ont été ajoutés au schéma WordprocessingML au format Open XML.</span><span class="sxs-lookup"><span data-stu-id="c87f7-234">The following elements were added to the WordprocessingML Open XML File Format schema.</span></span>
  
<span data-ttu-id="c87f7-235">**Tableau 1. Nouveaux éléments dans le schéma WordprocessingML au format Open XML pour les contrôles de contenu**</span><span class="sxs-lookup"><span data-stu-id="c87f7-235">**Table 1. New elements in the WordprocessingML Open XML File Format schema for content controls**</span></span>

|<span data-ttu-id="c87f7-236">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c87f7-236">**Element**</span></span>|<span data-ttu-id="c87f7-237">**Description**</span><span class="sxs-lookup"><span data-stu-id="c87f7-237">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c87f7-238">\<w:appearance\></span><span class="sxs-lookup"><span data-stu-id="c87f7-238">\<w:appearance\></span></span>  <br/> |<span data-ttu-id="c87f7-239">\<w:appearance\> est un élément enfant de \<w:sdtPr\>.</span><span class="sxs-lookup"><span data-stu-id="c87f7-239">\<w:appearance\> is a child element of \<w:sdtPr\>.</span></span>  <br/> <span data-ttu-id="c87f7-240">Voici les valeurs valides pour l’attribut val :</span><span class="sxs-lookup"><span data-stu-id="c87f7-240">The following values are valid for the val attribute:</span></span>  <br/> <span data-ttu-id="c87f7-241">\<w:appearance val= boundingBox</span><span class="sxs-lookup"><span data-stu-id="c87f7-241">\<w:appearance val= boundingBox</span></span>|<span data-ttu-id="c87f7-242">étiquettes</span><span class="sxs-lookup"><span data-stu-id="c87f7-242">tags</span></span>|<span data-ttu-id="c87f7-243">hidden.</span><span class="sxs-lookup"><span data-stu-id="c87f7-243">hidden.</span></span>  <br/> <span data-ttu-id="c87f7-244">La valeur par défaut est boundingBox.</span><span class="sxs-lookup"><span data-stu-id="c87f7-244">The default value is boundingBox.</span></span>  <br/> |
|<span data-ttu-id="c87f7-245">\<w:color\></span><span class="sxs-lookup"><span data-stu-id="c87f7-245">\<w:color\></span></span>  <br/> |<span data-ttu-id="c87f7-246">\<w:color\> est un élément enfant de \<w:sdtPr\>.</span><span class="sxs-lookup"><span data-stu-id="c87f7-246">\<w:color\> is a child element of \<w:sdtPr\>.</span></span>  <br/> <span data-ttu-id="c87f7-p113">Le modèle de contenu correspond au type complexe CT_Color existant. La valeur par défaut est la couleur utilisée dans Word 2010.</span><span class="sxs-lookup"><span data-stu-id="c87f7-p113">The content model matches the existing CT_Color complex type. The default value is the color used in Word 2010.</span></span>  <br/> |
   
## <a name="new-word-2013-content-control-object-model-members"></a><span data-ttu-id="c87f7-249">Nouveaux membres du modèle objet contrôle de contenu Word 2013</span><span class="sxs-lookup"><span data-stu-id="c87f7-249">New Word 2013 content control object model members</span></span>
<span data-ttu-id="c87f7-250"><a name="WordCC_NewOM"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-250"></span></span>

<span data-ttu-id="c87f7-251">Avec les nouvelles améliorations et les ajouts apportés aux contrôles de contenu dans Word 2013, le modèle objet Word a été mis à jour pour permettre la manipulation programmatique du nouveau jeu de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="c87f7-251">With the new enhancements and additions to content controls in Word 2013, the object model for Word has been updated to allow for programmatic manipulation of the new feature set.</span></span> <span data-ttu-id="c87f7-252">Par ailleurs, des modifications ont été apportées au format de fichier Open XML sous-jacent pour les documents de traitement de texte.</span><span class="sxs-lookup"><span data-stu-id="c87f7-252">In addition, changes have also been made to the underlying Open XML File Format for word processing documents.</span></span>
  
<span data-ttu-id="c87f7-253">Les sections suivantes fournissent davantage d’informations sur les modifications spécifiques apportées au modèle objet relatives à l’amélioration de chaque contrôle de contenu.</span><span class="sxs-lookup"><span data-stu-id="c87f7-253">The following sections provide more information about the specific object model changes related to each content control enhancement.</span></span>
  
### <a name="visualization-enhancements"></a><span data-ttu-id="c87f7-254">Améliorations de visualisation</span><span class="sxs-lookup"><span data-stu-id="c87f7-254">Visualization enhancements</span></span>
<span data-ttu-id="c87f7-255"><a name="WordCC_VisEnhancements"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-255"></span></span>

<span data-ttu-id="c87f7-256">Plusieurs ajouts de modèle objet sont inclus dans Word 2013 pour améliorer la visualisation du contrôle de contenu.</span><span class="sxs-lookup"><span data-stu-id="c87f7-256">Several object model additions are included in Word 2013 for content control visualization enhancements.</span></span> <span data-ttu-id="c87f7-257">Le tableau suivant répertorie les nouveaux membres de l’objet **ContentControl** pour la visualisation.</span><span class="sxs-lookup"><span data-stu-id="c87f7-257">The following table list new members of the **ContentControl** object for visualization.</span></span> 
  
<span data-ttu-id="c87f7-258">**Tableau 2. Nouveaux membres de l’objet ContentControl**</span><span class="sxs-lookup"><span data-stu-id="c87f7-258">**Table 2. New ContentControl object members**</span></span>

|<span data-ttu-id="c87f7-259">**Membre**</span><span class="sxs-lookup"><span data-stu-id="c87f7-259">**Member**</span></span>|<span data-ttu-id="c87f7-260">**Description**</span><span class="sxs-lookup"><span data-stu-id="c87f7-260">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c87f7-261">.</span><span class="sxs-lookup"><span data-stu-id="c87f7-261"></span></span> <span data-ttu-id="c87f7-262">**Appearance** en tant que **WdContentControlAppearance**</span><span class="sxs-lookup"><span data-stu-id="c87f7-262">**Appearance** as **WdContentControlAppearance**</span></span> <br/> |<span data-ttu-id="c87f7-263">Obtient ou définit la visualisation du contrôle de contenu.</span><span class="sxs-lookup"><span data-stu-id="c87f7-263">Gets or sets the visualization of the content control.</span></span>  <br/> |
|<span data-ttu-id="c87f7-264">.</span><span class="sxs-lookup"><span data-stu-id="c87f7-264"></span></span> <span data-ttu-id="c87f7-265">**Color** en tant que **WdColor**</span><span class="sxs-lookup"><span data-stu-id="c87f7-265">**Color** as **WdColor**</span></span> <br/> |<span data-ttu-id="c87f7-266">Obtient ou définit la couleur du contrôle de contenu.</span><span class="sxs-lookup"><span data-stu-id="c87f7-266">Gets or sets the color of the content control.</span></span>  <br/> |
   
<span data-ttu-id="c87f7-267">Le tableau suivant répertorie les constantes dans la nouvelle énumération **WdContentControlAppearance**.</span><span class="sxs-lookup"><span data-stu-id="c87f7-267">The following table lists constants in the new **WdContentControlAppearance** enumeration.</span></span> 
  
<span data-ttu-id="c87f7-268">**Tableau 3. Nouvelles constantes d’énumération WdContentControlAppearance**</span><span class="sxs-lookup"><span data-stu-id="c87f7-268">**Table 3. New WdContentControlAppearance enumeration constants**</span></span>

|<span data-ttu-id="c87f7-269">**Constante**</span><span class="sxs-lookup"><span data-stu-id="c87f7-269">**Constant**</span></span>|<span data-ttu-id="c87f7-270">**Description**</span><span class="sxs-lookup"><span data-stu-id="c87f7-270">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c87f7-271">**wdContentControlBoundingBox**</span><span class="sxs-lookup"><span data-stu-id="c87f7-271">**wdContentControlBoundingBox**</span></span> <br/> |<span data-ttu-id="c87f7-272">Représente un contrôle de contenu affiché sous la forme d’une zone ombrée rectangulaire/englobante (avec un titre facultatif).</span><span class="sxs-lookup"><span data-stu-id="c87f7-272">Represents a content control shown as a shaded rectangle/bounding box (with optional title).</span></span>  <br/> |
|<span data-ttu-id="c87f7-273">**wdContentControlTags**</span><span class="sxs-lookup"><span data-stu-id="c87f7-273">**wdContentControlTags**</span></span> <br/> |<span data-ttu-id="c87f7-274">Représente un contrôle de contenu affiché comme des marques de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="c87f7-274">Represents a content control shown as start/end markers.</span></span>  <br/> |
|<span data-ttu-id="c87f7-275">**wdContentControlHidden**</span><span class="sxs-lookup"><span data-stu-id="c87f7-275">**wdContentControlHidden**</span></span> <br/> |<span data-ttu-id="c87f7-276">Représente un contrôle de contenu qui n’est pas affiché.</span><span class="sxs-lookup"><span data-stu-id="c87f7-276">Represents a content control that is not shown.</span></span>  <br/> |
   
### <a name="code-sample"></a><span data-ttu-id="c87f7-277">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="c87f7-277">Code sample</span></span>
<span data-ttu-id="c87f7-278"><a name="WordCC_VisEnhancements"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-278"></span></span>

<span data-ttu-id="c87f7-279">L’exemple de code suivant montre comment créer des contrôles de contenu de texte enrichi et définir la visualisation par programme.</span><span class="sxs-lookup"><span data-stu-id="c87f7-279">The following code sample shows how to create rich text content controls and set visualization programmatically.</span></span>
  
```vb
Sub testVisualization()
   Dim objcc As ContentControl
   Dim objRange As Range
   
   ' Get the first paragraph as a range object.
   Set objRange = ActiveDocument.Paragraphs(1).Range
   ' Create a rich text content control around the first paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   objcc.Title = "Default Bounding Box"
   ' Set visualization to the default.
   objcc.Appearance = wdContentControlBoundingBox
   
   ' Create a new paragraph.
   objRange.InsertParagraphAfter
   Set objRange = ActiveDocument.Paragraphs(2).Range
   ' Create a rich text content control around the second paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   objcc.Title = "Non Bounding"
   ' Set visualization to invisible.
   objcc.Appearance = wdContentControlHidden
   
   ' Create a new paragraph.
   objRange.InsertParagraphAfter
   Set objRange = ActiveDocument.Paragraphs(3).Range
   ' Create a rich text content control around the third paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   objcc.Title = "Tags Only with Pink color"
   ' Set visualization to Start/End tags with pink color.
   objcc.Appearance = wdContentControlTags
   objcc.Color = wdColorPink
End Sub
```

### <a name="xml-mapping"></a><span data-ttu-id="c87f7-280">Mappage XML</span><span class="sxs-lookup"><span data-stu-id="c87f7-280">XML mapping</span></span>
<span data-ttu-id="c87f7-281"><a name="WordCC_XMLMappingOM"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-281"></span></span>

<span data-ttu-id="c87f7-282">Aucun ajout n’a été effectué au modèle objet Word 2013 pour prendre en charge le mappage de texte enrichi sur les nœuds XML dans le magasin de données du document.</span><span class="sxs-lookup"><span data-stu-id="c87f7-282">No additions were made to the Word 2013 object model to accommodate rich text mapping to XML nodes in the document data store.</span></span> <span data-ttu-id="c87f7-283">Utilisez plutôt le modèle objet existant pour mapper un contrôle de contenu de texte enrichi sur un nœud XML dans le magasin de données du document.</span><span class="sxs-lookup"><span data-stu-id="c87f7-283">Instead, use the existing object model to map a rich text content control to an XML node in the document data store.</span></span> <span data-ttu-id="c87f7-284">En outre, aucune modification n’a été apportée au schéma WordprocessingML du format de fichier Open XML sous-jacent dans le cadre de la nouvelle prise en charge du contrôle de contenu de texte enrichi spécifiquement pour le mappage XML.</span><span class="sxs-lookup"><span data-stu-id="c87f7-284">Additionally, no changes were made to the underlying Open XML File Format WordprocessingML schema as part of the newly included rich text content control support specifically for XML mapping.</span></span>
  
#### <a name="code-sample"></a><span data-ttu-id="c87f7-285">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="c87f7-285">Code sample</span></span>

<span data-ttu-id="c87f7-286">L’exemple de code suivant montre comment mapper un contrôle de contenu de texte enrichi à un nœud XML par programme.</span><span class="sxs-lookup"><span data-stu-id="c87f7-286">The following code sample shows how to map a rich text content control to an XML node programmatically.</span></span>
  
```vb
Sub testRichBinding()
   Dim objRange As Range
   Dim objcc As ContentControl
   Dim objCustomPart As CustomXMLPart
   Dim blnMap As Boolean
   
   ' Add a custom XML part to the data store.
   Set objCustomPart = ActiveDocument.CustomXMLParts.Add
   ' Load XML fragment into the custom XML part.
   objCustomPart.LoadXML ("<x>Rich Text Databinding</x>")
   ' Get the first paragraph as a range object.
   Set objRange = ActiveDocument.Paragraphs(1).Range
   ' Create a rich text content control around the first paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   ' Bind the XML node to the rich text content control.
   blnMap = objcc.XMLMapping.SetMapping("/x")
   ' Return whether mapping worked.
   MsgBox objcc.XMLMapping.IsMapped
End Sub
```

### <a name="repeating-section-content-controls-represented-in-the-object-model"></a><span data-ttu-id="c87f7-287">Contrôles de contenu répétitif représentés dans le modèle objet</span><span class="sxs-lookup"><span data-stu-id="c87f7-287">Repeating section content controls represented in the object model</span></span>
<span data-ttu-id="c87f7-288"><a name="WordCC_RepeatingSection"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-288"></span></span>

<span data-ttu-id="c87f7-p119">Le contrôle de contenu répétitif est disponible dans le modèle objet via les ajouts suivants apportés à l’objet **ContentControl** et les nouveaux objets **RepeatingSectionItem** et **RepeatingSectionItemColl**. Le tableau 4 répertorie les nouveaux membres les plus importants de l’objet **ContentControl** pour les contrôles de contenu répétitif.</span><span class="sxs-lookup"><span data-stu-id="c87f7-p119">The repeating section content control is available in the object model by using the following additions to the **ContentControl** object and the new **RepeatingSectionItem** and **RepeatingSectionItemColl** objects. Table 4 lists the most important new members of the **ContentControl** object for repeating section content controls.</span></span> 
  
<span data-ttu-id="c87f7-291">**Tableau 4. Membres de l’objet ContentControl**</span><span class="sxs-lookup"><span data-stu-id="c87f7-291">**Table 4. ContentControl object members**</span></span>

|<span data-ttu-id="c87f7-292">**Membre**</span><span class="sxs-lookup"><span data-stu-id="c87f7-292">**Member**</span></span>|<span data-ttu-id="c87f7-293">**Description**</span><span class="sxs-lookup"><span data-stu-id="c87f7-293">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c87f7-294">**AllowInsertDeleteSection** en tant que **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c87f7-294">**AllowInsertDeleteSection** as **Boolean**</span></span> <br/> |<span data-ttu-id="c87f7-295">Indique si les utilisateurs peuvent ajouter ou supprimer des sections du contrôle de contenu à l’aide de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c87f7-295">Gets or sets whether users can add or remove sections from the content control by using the UI.</span></span> <span data-ttu-id="c87f7-296">Si cette propriété est appelée pour un contrôle de contenu qui n’est pas de type répétitif, l’appel échoue avec le message d’erreur suivant : « Cette propriété peut uniquement être utilisée avec des contrôles de contenu répétitifs. »</span><span class="sxs-lookup"><span data-stu-id="c87f7-296">If this property is called for a content control that is not of type repeating section, the call fails with the following error message: "This property can only be used with repeating section content controls."</span></span>  <br/> |
|<span data-ttu-id="c87f7-297">**RepeatingSectionItemTitle** en tant que **String**</span><span class="sxs-lookup"><span data-stu-id="c87f7-297">**RepeatingSectionItemTitle** as **String**</span></span> <br/> |<span data-ttu-id="c87f7-298">Obtient ou définit le nom des éléments répétitifs utilisé dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="c87f7-298">Gets or sets the name of repeating section items used in the context menu.</span></span> <span data-ttu-id="c87f7-299">Si cette propriété est appelée pour un contrôle de contenu qui n’est pas de type répétitif, l’appel échoue avec le message d’erreur suivant : « Cette propriété peut uniquement être utilisée avec des contrôles de contenu répétitifs. »</span><span class="sxs-lookup"><span data-stu-id="c87f7-299">If this property is called for a content control that is not of type repeating section, the call fails with: "This property can only be used with repeating section content controls."</span></span>  <br/> |
|<span data-ttu-id="c87f7-300">**InsertRepeatingSectionItemBefore** en tant que **ContentControl**</span><span class="sxs-lookup"><span data-stu-id="c87f7-300">**InsertRepeatingSectionItemBefore** as **ContentControl**</span></span> <br/> |<span data-ttu-id="c87f7-301">Ajoute un élément répétitif avant l’élément actuel et renvoie le nouvel élément répétitif.</span><span class="sxs-lookup"><span data-stu-id="c87f7-301">Adds a repeating section item before the current item and returns the new repeating section item.</span></span> <span data-ttu-id="c87f7-302">Si cette méthode est appelée pour un contrôle de contenu qui n’est pas de type répétitif, l’appel échoue avec le message d’erreur suivant : « Cette propriété peut uniquement être utilisée avec des contrôles de contenu répétitifs. »</span><span class="sxs-lookup"><span data-stu-id="c87f7-302">If this method is called for a content control that is not of type repeating section item, the call fails with: "This property can only be used with repeating section item content controls."</span></span>  <br/> |
|<span data-ttu-id="c87f7-303">**InsertRepeatingSectionItemAfter** en tant que **ContentControl**</span><span class="sxs-lookup"><span data-stu-id="c87f7-303">**InsertRepeatingSectionItemAfter** as **ContentControl**</span></span> <br/> |<span data-ttu-id="c87f7-304">Ajoute un élément répétitif après l’élément actuel et renvoie le nouvel élément répétitif.</span><span class="sxs-lookup"><span data-stu-id="c87f7-304">Adds a repeating section item after the current item and returns the new repeating section item.</span></span> <span data-ttu-id="c87f7-305">Si cette méthode est appelée pour un contrôle de contenu qui n’est pas de type répétitif, l’appel échoue avec le message d’erreur suivant : « Cette propriété peut uniquement être utilisée avec des contrôles de contenu répétitifs. »</span><span class="sxs-lookup"><span data-stu-id="c87f7-305">If this method is called for a content control that is not of type repeating section item, the call fails with: "This property can only be used with repeating section item content controls."</span></span>  <br/> |
   
<span data-ttu-id="c87f7-306">Le tableau 5 répertorie les membres les plus importants de l’objet **RepeatingSectionItem**.</span><span class="sxs-lookup"><span data-stu-id="c87f7-306">Table 5 lists the most important members of the **RepeatingSectionItem** object.</span></span> 
  
<span data-ttu-id="c87f7-307">**Tableau 5. Membres de l’objet RepeatingSectionItem**</span><span class="sxs-lookup"><span data-stu-id="c87f7-307">**Table 5. RepeatingSectionItem object members**</span></span>

|<span data-ttu-id="c87f7-308">**Membre**</span><span class="sxs-lookup"><span data-stu-id="c87f7-308">**Member**</span></span>|<span data-ttu-id="c87f7-309">**Description**</span><span class="sxs-lookup"><span data-stu-id="c87f7-309">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c87f7-310">**Range** en tant que **Range**</span><span class="sxs-lookup"><span data-stu-id="c87f7-310">**Range** as **Range**</span></span> <br/> |<span data-ttu-id="c87f7-311">Renvoie la plage de l’élément répétitif spécifié, à l’exclusion des balises de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="c87f7-311">Returns the range of the specified repeating section item, excluding the start and end tags.</span></span>  <br/> |
|<span data-ttu-id="c87f7-312">**Delete**</span><span class="sxs-lookup"><span data-stu-id="c87f7-312">**Delete**</span></span> <br/> |<span data-ttu-id="c87f7-313">Supprime l’élément répétitif spécifié.</span><span class="sxs-lookup"><span data-stu-id="c87f7-313">Deletes the specified repeating section item.</span></span>  <br/> |
|<span data-ttu-id="c87f7-314">**InsertItemAfter** en tant que **RepeatingSectionItem**</span><span class="sxs-lookup"><span data-stu-id="c87f7-314">**InsertItemAfter** as **RepeatingSectionItem**</span></span> <br/> |<span data-ttu-id="c87f7-315">Ajoute un élément répétitif après l’élément spécifié et renvoie le nouvel élément.</span><span class="sxs-lookup"><span data-stu-id="c87f7-315">Adds a repeating section item after the specified item and returns the new item.</span></span>  <br/> |
|<span data-ttu-id="c87f7-316">**InsertItemBefore** en tant que **RepeatingSectionItem**</span><span class="sxs-lookup"><span data-stu-id="c87f7-316">**InsertItemBefore** as **RepeatingSectionItem**</span></span> <br/> |<span data-ttu-id="c87f7-317">Ajoute un élément répétitif avant l’élément spécifié et renvoie le nouvel élément.</span><span class="sxs-lookup"><span data-stu-id="c87f7-317">Adds a repeating section item before the specified item and returns the new item.</span></span>  <br/> |
   
<span data-ttu-id="c87f7-318">Le tableau 6 répertorie les membres les plus importants de l’objet **RepeatingSectionItemColl**.</span><span class="sxs-lookup"><span data-stu-id="c87f7-318">Table 6 lists the most important members of the **RepeatingSectionItemColl** object.</span></span> 
  
<span data-ttu-id="c87f7-319">**Tableau 6. Membres de l’objet RepeatingSectionItemColl**</span><span class="sxs-lookup"><span data-stu-id="c87f7-319">**Table 6. RepeatingSectionItemColl object members**</span></span>

|<span data-ttu-id="c87f7-320">**Membre**</span><span class="sxs-lookup"><span data-stu-id="c87f7-320">**Member**</span></span>|<span data-ttu-id="c87f7-321">**Description**</span><span class="sxs-lookup"><span data-stu-id="c87f7-321">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c87f7-322">**Item** en tant que **RepeatingSectionItem**</span><span class="sxs-lookup"><span data-stu-id="c87f7-322">**Item** as **RepeatingSectionItem**</span></span> <br/> |<span data-ttu-id="c87f7-323">Renvoie un élément répétitif individuel.</span><span class="sxs-lookup"><span data-stu-id="c87f7-323">Returns an individual repeating section item.</span></span>  <br/> |
   
<span data-ttu-id="c87f7-324">Le tableau 7 illustre le nouveau membre de l’énumération **WdContentControlType** pour les contrôles de contenu répétitif.</span><span class="sxs-lookup"><span data-stu-id="c87f7-324">Table 7 shows the new member of the **WdContentControlType** enumeration for repeating section content controls.</span></span> 
  
<span data-ttu-id="c87f7-325">**Tableau 7. Ajout à l’énumération WdContentControlType**</span><span class="sxs-lookup"><span data-stu-id="c87f7-325">**Table 7. WdContentControlType enumeration addition**</span></span>

|<span data-ttu-id="c87f7-326">**Constante**</span><span class="sxs-lookup"><span data-stu-id="c87f7-326">**Constant**</span></span>|<span data-ttu-id="c87f7-327">**Description**</span><span class="sxs-lookup"><span data-stu-id="c87f7-327">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c87f7-328">**wdContentControlRepeatingSection**</span><span class="sxs-lookup"><span data-stu-id="c87f7-328">**wdContentControlRepeatingSection**</span></span> <br/> |<span data-ttu-id="c87f7-329">Représente un contrôle de contenu qui contient un seul élément dans une section répétitive.</span><span class="sxs-lookup"><span data-stu-id="c87f7-329">Represents a content control that contains a single item in a repeating section.</span></span>  <br/> |
   
### <a name="code-sample"></a><span data-ttu-id="c87f7-330">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="c87f7-330">Code sample</span></span>
<span data-ttu-id="c87f7-331"><a name="WordCC_RepeatingSection"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-331"></span></span>

<span data-ttu-id="c87f7-332">L’exemple de code suivant montre comment utiliser par programme des contrôles de contenu répétitif.</span><span class="sxs-lookup"><span data-stu-id="c87f7-332">The following code sample shows how to use repeating section content controls programmatically.</span></span>
  
```vb
Sub testRepeatingSectionControl()
   Dim objRange As Range
   Dim objTable As Table
   Dim objCustomPart As CustomXMLPart
   Dim objCC As ContentControl
   Dim objCustomNode As CustomXMLNode
   
   Set objCustomPart = ActiveDocument.CustomXMLParts.Add
   objCustomPart.LoadXML ("<books>" & _
       "<book><title>Everyday Italian</title>" & _
       "<author>Giada De Laurentiis</author></book>" & _
       "<book><title>Harry Potter</title>" & _
       "<author>J K. Rowling</author></book>" & _
       "<book><title>Learning XML</title>" & _
       "<author>Erik T. Ray</author></book></books>")
   
   Set objRange = ActiveDocument.Paragraphs(1).Range
   Set objTable = ActiveDocument.Tables.Add(objRange, 2, 2)
   With objTable.Borders
       .InsideLineStyle = wdLineStyleSingle
       .OutsideLineStyle = wdLineStyleDouble
   End With
   Set objRange = objTable.Cell(1, 1).Range
   Set objCustomNode = objCustomPart.SelectSingleNode("/books[1]/book[1]/title[1]")
   Set objCC = ActiveDocument.ContentControls.Add(wdContentControlText, objRange)
   objCC.XMLMapping.SetMappingByNode objCustomNode
   Set objRange = objTable.Cell(1, 2).Range
   Set objCustomNode = objCustomPart.SelectSingleNode("/books[1]/book[1]/author[1]")
   Set objCC = ActiveDocument.ContentControls.Add(wdContentControlText, objRange)
   objCC.XMLMapping.SetMappingByNode objCustomNode
   Set objRange = objTable.Rows(1).Range
   Set objCC = ActiveDocument.ContentControls.Add(wdContentControlRepeatingSection, objRange)
   objCC.XMLMapping.SetMapping ("/books[1]/book")
End Sub
```

### <a name="open-xml-file-format-changes-for-repeating-section-content-controls"></a><span data-ttu-id="c87f7-333">Modifications de format de fichier Open XML pour les contrôles de contenu répétitif</span><span class="sxs-lookup"><span data-stu-id="c87f7-333">Open XML File Format changes for repeating section content controls</span></span>
<span data-ttu-id="c87f7-334"><a name="WordCC_RepeatingSection"> </a></span><span class="sxs-lookup"><span data-stu-id="c87f7-334"></span></span>

<span data-ttu-id="c87f7-335">La représentation de format de fichier d’un contrôle du contenu répétitif utilise généralement les mêmes noms, valeurs, etc. pour les éléments, comme le balisage XML existant ; cependant, l’élément \<sdt\> représentant le conteneur de la section répétitive extérieure se trouve dans l’espace de noms Word 2013, pour assurer la compatibilité avec les versions antérieures de Word.</span><span class="sxs-lookup"><span data-stu-id="c87f7-335">The file format representation of a repeating section content control generally uses the same element names, values, and so on as the existing XML markup; however, the \<sdt\> element representing the outer repeating section container exists in the Word 2013 namespace, to ensure compatibility with earlier versions of Word.</span></span>
  
<span data-ttu-id="c87f7-p124">Les éléments répétitifs individuels dans le contrôle de contenu répétitif (qui entourent chaque élément) sont enregistrés en tant que contrôles de contenu de texte enrichi à l’aide de la représentation WordprocessingML existante. Le tableau 8 répertorie les nouveaux éléments dans le schéma WordprocessingML pour les contrôles de contenu répétitif.</span><span class="sxs-lookup"><span data-stu-id="c87f7-p124">The individual repeating items within the repeating section content control (that surround each individual item) are saved as rich text content controls using the existing WordprocessingML representation. Table 8 lists new elements in the WordprocessingML schema for repeating section content controls.</span></span>
  
<span data-ttu-id="c87f7-338">**Tableau 8. Nouveaux éléments dans le schéma WordprocessingML pour les contrôles de contenu répétitif**</span><span class="sxs-lookup"><span data-stu-id="c87f7-338">**Table 8. New elements in the WordprocessingML schema for repeating section content controls**</span></span>

|<span data-ttu-id="c87f7-339">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c87f7-339">**Element**</span></span>|<span data-ttu-id="c87f7-340">**Description**</span><span class="sxs-lookup"><span data-stu-id="c87f7-340">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c87f7-341">\<w15:repeatingSection\></span><span class="sxs-lookup"><span data-stu-id="c87f7-341">\<w15:repeatingSection\></span></span>  <br/> |<span data-ttu-id="c87f7-p125">Spécifie un contrôle de contenu répétitif. Cet élément est incompatible avec tous les autres types de contrôles et n’a ni attributs enfants, ni éléments.</span><span class="sxs-lookup"><span data-stu-id="c87f7-p125">Specifies a repeating section content control. This element is mutually exclusive with all other control types and has no child elements or attributes.</span></span>  <br/> |
|<span data-ttu-id="c87f7-344">\<w15:repeatingSectionItem\></span><span class="sxs-lookup"><span data-stu-id="c87f7-344">\<w15:repeatingSectionItem\></span></span>  <br/> |<span data-ttu-id="c87f7-p126">Spécifie un contrôle de contenu d’élément répétitif. Cet élément est incompatible avec tous les autres types de contrôles et n’a ni attributs enfants, ni éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="c87f7-p126">Specifies a repeating section item content control. This element is mutually exclusive with all other control types, and has no child elements or attributes.</span></span>  <br/> |
|<span data-ttu-id="c87f7-347">\<w15:doNotAllowInsertDeleteSection\></span><span class="sxs-lookup"><span data-stu-id="c87f7-347">\<w15:doNotAllowInsertDeleteSection\></span></span>  <br/> |<span data-ttu-id="c87f7-348">Spécifie que l’utilisateur ne peut ni ajouter ni supprimer des sections à l’aide des options de l’interface dans Word 2013.</span><span class="sxs-lookup"><span data-stu-id="c87f7-348">Specifies that the user cannot add or delete sections by using the user interface in Word 2013.</span></span>  <br/> |
|<span data-ttu-id="c87f7-349">\<w15:sectionTitle\></span><span class="sxs-lookup"><span data-stu-id="c87f7-349">\<w15:sectionTitle\></span></span>  <br/> |<span data-ttu-id="c87f7-350">Spécifie le nom des éléments de section répétitive (et est utilisé dans le menu contextuel lorsque le contrôle est sélectionné).</span><span class="sxs-lookup"><span data-stu-id="c87f7-350">Specifies the name of repeating section items (and is used in the context menu when the control is chosen).</span></span>  <br/> |
   

  

