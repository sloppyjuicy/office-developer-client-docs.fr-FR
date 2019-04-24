---
title: Variables de modèle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Les instances de variables de modèle (représentées par un élément templateVariable) spécifient les données d'un élément de flux d'activités dans un modèle d'activité.
ms.openlocfilehash: 9b37665488f0f1e2bd205fb7d4a5d2201697d7c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329175"
---
# <a name="template-variables"></a><span data-ttu-id="8a303-103">Variables de modèle</span><span class="sxs-lookup"><span data-stu-id="8a303-103">Template variables</span></span>

<span data-ttu-id="8a303-104">Les instances de variables de modèle (représentées par un élément **templateVariable** ) spécifient les données d'un élément de flux d'activités dans un modèle d'activité.</span><span class="sxs-lookup"><span data-stu-id="8a303-104">Instances of template variables (represented by a **templateVariable** element) specify the data of an activity feed item in an activity template.</span></span> 
  
<span data-ttu-id="8a303-105">Pour obtenir un exemple de XML d'informations sur les activités, voir [exemple de XML](activity-feed-xml-example.md)d'informations sur les activités.</span><span class="sxs-lookup"><span data-stu-id="8a303-105">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>

<span data-ttu-id="8a303-106">Le tableau suivant présente les types de variables de modèle prises en charge, chacune étant représentée par la valeur d'énumération XML correspondante.</span><span class="sxs-lookup"><span data-stu-id="8a303-106">The following table shows the types of supported template variables, each represented by the corresponding XML enumeration value.</span></span>
  
|<span data-ttu-id="8a303-107">**Type de variable de modèle**</span><span class="sxs-lookup"><span data-stu-id="8a303-107">**Type of template variable**</span></span>|<span data-ttu-id="8a303-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="8a303-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a303-109">**entityVariable**</span><span class="sxs-lookup"><span data-stu-id="8a303-109">**entityVariable**</span></span> <br/> |<span data-ttu-id="8a303-110">Une personne, un groupe ou un élément.</span><span class="sxs-lookup"><span data-stu-id="8a303-110">A person, group, or thing.</span></span>  <br/> |
|<span data-ttu-id="8a303-111">**linkVariable**</span><span class="sxs-lookup"><span data-stu-id="8a303-111">**linkVariable**</span></span> <br/> |<span data-ttu-id="8a303-112">Un lien.</span><span class="sxs-lookup"><span data-stu-id="8a303-112">A link.</span></span>  <br/> |
|<span data-ttu-id="8a303-113">**listVariable**</span><span class="sxs-lookup"><span data-stu-id="8a303-113">**listVariable**</span></span> <br/> |<span data-ttu-id="8a303-114">Groupe d'objets.</span><span class="sxs-lookup"><span data-stu-id="8a303-114">A group of objects.</span></span>  <br/> |
|<span data-ttu-id="8a303-115">**pictureVariable**</span><span class="sxs-lookup"><span data-stu-id="8a303-115">**pictureVariable**</span></span> <br/> |<span data-ttu-id="8a303-116">Image.</span><span class="sxs-lookup"><span data-stu-id="8a303-116">A picture.</span></span>  <br/> |
|<span data-ttu-id="8a303-117">**publisherVariable**</span><span class="sxs-lookup"><span data-stu-id="8a303-117">**publisherVariable**</span></span> <br/> |<span data-ttu-id="8a303-118">Éditeur de l'élément de flux d'activités.</span><span class="sxs-lookup"><span data-stu-id="8a303-118">The publisher of the activity feed item.</span></span>  <br/> |
|<span data-ttu-id="8a303-119">**textVariable**</span><span class="sxs-lookup"><span data-stu-id="8a303-119">**textVariable**</span></span> <br/> |<span data-ttu-id="8a303-120">Bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="8a303-120">A block of text.</span></span>  <br/> |
   
<span data-ttu-id="8a303-121">Chaque type de variable de modèle comporte des éléments requis pour spécifier les données relatives à cette variable.</span><span class="sxs-lookup"><span data-stu-id="8a303-121">Each type of template variable has required elements to specify the data about that variable.</span></span> <span data-ttu-id="8a303-122">Les variables de modèle sont spécifiées comme suit:</span><span class="sxs-lookup"><span data-stu-id="8a303-122">Template variables are specified as follows:</span></span>
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a><span data-ttu-id="8a303-123">Variable de modèle de liste</span><span class="sxs-lookup"><span data-stu-id="8a303-123">List template variable</span></span>

<span data-ttu-id="8a303-124">Vous pouvez spécifier des variables de modèle qui sont contenues dans une liste (délimitées par les éléments **listVariable** et **ListItems** ) comme suit:</span><span class="sxs-lookup"><span data-stu-id="8a303-124">You can specify template variables that are contained within a list (delimited by the **listVariable** and **listItems** elements) as follows:</span></span> 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
<span data-ttu-id="8a303-125">Une variable de modèle du type **listVariable** est un conteneur d'objets.</span><span class="sxs-lookup"><span data-stu-id="8a303-125">A template variable of the **listVariable** type is a container for objects.</span></span> <span data-ttu-id="8a303-126">Il peut contenir des éléments délimités par des virgules (du type **LinkVariable** ou **textVariable** ) ou des images (du type **pictureVariable** ).</span><span class="sxs-lookup"><span data-stu-id="8a303-126">It can contain comma-delimited items (of the **linkVariable** or **textVariable** type) or pictures (of the **pictureVariable** type).</span></span> <span data-ttu-id="8a303-127">Les listes peuvent contenir jusqu'à cinq éléments de lien, cinq éléments de texte ou cinq images.</span><span class="sxs-lookup"><span data-stu-id="8a303-127">Lists can contain up to five link items, five text items, or five pictures.</span></span> 
  
<span data-ttu-id="8a303-128">Outlook Social Connector (OSC) localise les éléments de liste de liens ou de texte en fonction des paramètres régionaux du système Windows.</span><span class="sxs-lookup"><span data-stu-id="8a303-128">The Outlook Social Connector (OSC) localizes link or text list items according to the Windows system locale.</span></span>
  
<span data-ttu-id="8a303-129">Pour analyser et afficher correctement les images d'un élément de flux d'activité, vous devez inclure des images dans une liste.</span><span class="sxs-lookup"><span data-stu-id="8a303-129">To correctly parse and display pictures in an activity feed item, you must include pictures in a list.</span></span> <span data-ttu-id="8a303-130">Toutes les images sont redimensionnées pour avoir une hauteur de 52 pixels.</span><span class="sxs-lookup"><span data-stu-id="8a303-130">All pictures are resized to be 52 pixels high.</span></span> <span data-ttu-id="8a303-131">La largeur de l'image n'est pas redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="8a303-131">The width of the picture is not resized.</span></span>
  
## <a name="template-variable-elements"></a><span data-ttu-id="8a303-132">Éléments de variable de modèle</span><span class="sxs-lookup"><span data-stu-id="8a303-132">Template variable elements</span></span>

<span data-ttu-id="8a303-133">Cette section traite des éléments obligatoires et facultatifs pris en charge pour chaque type de variable de modèle.</span><span class="sxs-lookup"><span data-stu-id="8a303-133">This section covers the required and optional elements supported for each type of template variable.</span></span>
  
### <a name="entityvariable"></a><span data-ttu-id="8a303-134">entityVariable</span><span class="sxs-lookup"><span data-stu-id="8a303-134">entityVariable</span></span>

|<span data-ttu-id="8a303-135">**Élément**</span><span class="sxs-lookup"><span data-stu-id="8a303-135">**Element**</span></span>|<span data-ttu-id="8a303-136">**Description**</span><span class="sxs-lookup"><span data-stu-id="8a303-136">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a303-137">**nom**</span><span class="sxs-lookup"><span data-stu-id="8a303-137">**name**</span></span> <br/> |<span data-ttu-id="8a303-138">Nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="8a303-138">The name of the variable.</span></span> <span data-ttu-id="8a303-139">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8a303-139">Required.</span></span>  <br/> |
|<span data-ttu-id="8a303-140">**id**</span><span class="sxs-lookup"><span data-stu-id="8a303-140">**id**</span></span> <br/> |<span data-ttu-id="8a303-141">ID unique de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8a303-141">The unique ID of the user.</span></span> <span data-ttu-id="8a303-142">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8a303-142">Required.</span></span>  <br/> |
|<span data-ttu-id="8a303-143">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="8a303-143">**nameHint**</span></span> <br/> |<span data-ttu-id="8a303-144">Nom à afficher dans l'élément de flux.</span><span class="sxs-lookup"><span data-stu-id="8a303-144">The name to be displayed in the feed item.</span></span> <span data-ttu-id="8a303-145">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8a303-145">Optional.</span></span>  <br/> |
|<span data-ttu-id="8a303-146">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="8a303-146">**profileUrl**</span></span> <br/> |<span data-ttu-id="8a303-147">URL du profil de la personne qui sera utilisée comme lien hypertexte pour le nom de la personne dans l'élément de flux, si le nom de la personne est présent.</span><span class="sxs-lookup"><span data-stu-id="8a303-147">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="8a303-148">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8a303-148">Optional.</span></span>  <br/> |
|<span data-ttu-id="8a303-149">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="8a303-149">**emailAddress**</span></span> <br/> |<span data-ttu-id="8a303-150">Adresse de messagerie utilisée pour mettre à jour les informations de contact de cette personne dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="8a303-150">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="8a303-151">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8a303-151">Optional.</span></span>  <br/> |
   
### <a name="linkvariable"></a><span data-ttu-id="8a303-152">linkVariable</span><span class="sxs-lookup"><span data-stu-id="8a303-152">linkVariable</span></span>

|<span data-ttu-id="8a303-153">**Élément**</span><span class="sxs-lookup"><span data-stu-id="8a303-153">**Element**</span></span>|<span data-ttu-id="8a303-154">**Description**</span><span class="sxs-lookup"><span data-stu-id="8a303-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a303-155">**nom**</span><span class="sxs-lookup"><span data-stu-id="8a303-155">**name**</span></span> <br/> |<span data-ttu-id="8a303-156">Nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="8a303-156">The name of the variable.</span></span> <span data-ttu-id="8a303-157">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8a303-157">Required.</span></span>  <br/> |
|<span data-ttu-id="8a303-158">**value**</span><span class="sxs-lookup"><span data-stu-id="8a303-158">**value**</span></span> <br/> |<span data-ttu-id="8a303-159">URL de ce lien.</span><span class="sxs-lookup"><span data-stu-id="8a303-159">The URL for this link.</span></span> <span data-ttu-id="8a303-160">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8a303-160">Required.</span></span>  <br/> |
|<span data-ttu-id="8a303-161">**text**</span><span class="sxs-lookup"><span data-stu-id="8a303-161">**text**</span></span> <br/> |<span data-ttu-id="8a303-162">Texte du lien à afficher à la place de l'URL proprement dite.</span><span class="sxs-lookup"><span data-stu-id="8a303-162">The link text to display instead of the URL itself.</span></span> <span data-ttu-id="8a303-163">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8a303-163">Optional.</span></span>  <br/> |
   
### <a name="listvariable"></a><span data-ttu-id="8a303-164">listVariable</span><span class="sxs-lookup"><span data-stu-id="8a303-164">listVariable</span></span>

|<span data-ttu-id="8a303-165">**Élément**</span><span class="sxs-lookup"><span data-stu-id="8a303-165">**Element**</span></span>|<span data-ttu-id="8a303-166">**Description**</span><span class="sxs-lookup"><span data-stu-id="8a303-166">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a303-167">**nom**</span><span class="sxs-lookup"><span data-stu-id="8a303-167">**name**</span></span> <br/> |<span data-ttu-id="8a303-168">Nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="8a303-168">The name of the variable.</span></span> <span data-ttu-id="8a303-169">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8a303-169">Required.</span></span>  <br/> |
|<span data-ttu-id="8a303-170">**listItems**</span><span class="sxs-lookup"><span data-stu-id="8a303-170">**listItems**</span></span> <br/> |<span data-ttu-id="8a303-171">Conteneur pour les éléments de la liste.</span><span class="sxs-lookup"><span data-stu-id="8a303-171">A container for items in the list.</span></span> <span data-ttu-id="8a303-172">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8a303-172">Required.</span></span>  <br/> |
   
### <a name="picturevariable"></a><span data-ttu-id="8a303-173">pictureVariable</span><span class="sxs-lookup"><span data-stu-id="8a303-173">pictureVariable</span></span>

|<span data-ttu-id="8a303-174">**Élément**</span><span class="sxs-lookup"><span data-stu-id="8a303-174">**Element**</span></span>|<span data-ttu-id="8a303-175">**Description**</span><span class="sxs-lookup"><span data-stu-id="8a303-175">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a303-176">**nom**</span><span class="sxs-lookup"><span data-stu-id="8a303-176">**name**</span></span> <br/> |<span data-ttu-id="8a303-177">Nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="8a303-177">The name of the variable.</span></span> <span data-ttu-id="8a303-178">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8a303-178">Required.</span></span>  <br/> |
|<span data-ttu-id="8a303-179">**value**</span><span class="sxs-lookup"><span data-stu-id="8a303-179">**value**</span></span> <br/> |<span data-ttu-id="8a303-180">URL de l'image.</span><span class="sxs-lookup"><span data-stu-id="8a303-180">The URL for the picture.</span></span> <span data-ttu-id="8a303-181">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8a303-181">Required.</span></span>  <br/> |
|<span data-ttu-id="8a303-182">**altText**</span><span class="sxs-lookup"><span data-stu-id="8a303-182">**altText**</span></span> <br/> |<span data-ttu-id="8a303-183">Texte de remplacement à afficher pour l'accessibilité et lorsque l'utilisateur déplace le pointeur de la souris sur l'image.</span><span class="sxs-lookup"><span data-stu-id="8a303-183">The alternate text to display for accessibility and when the user moves the mouse pointer over the picture.</span></span> <span data-ttu-id="8a303-184">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8a303-184">Optional.</span></span>  <br/> |
|<span data-ttu-id="8a303-185">**href**</span><span class="sxs-lookup"><span data-stu-id="8a303-185">**href**</span></span> <br/> |<span data-ttu-id="8a303-186">Lien hypertexte à utiliser lorsque l'utilisateur clique sur l'image, si la cible souhaitée n'est pas l'URL de l'image spécifiée par l'élément **value** .</span><span class="sxs-lookup"><span data-stu-id="8a303-186">The hyperlink to use when the user clicks the picture, if the desired target is not the picture URL specified by the **value** element.</span></span> <span data-ttu-id="8a303-187">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8a303-187">Optional.</span></span>  <br/> |
   
### <a name="publishervariable"></a><span data-ttu-id="8a303-188">publisherVariable</span><span class="sxs-lookup"><span data-stu-id="8a303-188">publisherVariable</span></span>

|<span data-ttu-id="8a303-189">**Élément**</span><span class="sxs-lookup"><span data-stu-id="8a303-189">**Element**</span></span>|<span data-ttu-id="8a303-190">**Description**</span><span class="sxs-lookup"><span data-stu-id="8a303-190">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a303-191">**nom**</span><span class="sxs-lookup"><span data-stu-id="8a303-191">**name**</span></span> <br/> |<span data-ttu-id="8a303-192">Nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="8a303-192">The name of the variable.</span></span> <span data-ttu-id="8a303-193">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8a303-193">Required.</span></span>  <br/> |
|<span data-ttu-id="8a303-194">**id**</span><span class="sxs-lookup"><span data-stu-id="8a303-194">**id**</span></span> <br/> |<span data-ttu-id="8a303-195">ID unique de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8a303-195">The unique ID of the user.</span></span> <span data-ttu-id="8a303-196">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8a303-196">Required.</span></span>  <br/> |
|<span data-ttu-id="8a303-197">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="8a303-197">**nameHint**</span></span> <br/> |<span data-ttu-id="8a303-198">Nom à afficher dans l'élément de flux.</span><span class="sxs-lookup"><span data-stu-id="8a303-198">The name to be displayed in the feed item.</span></span> <span data-ttu-id="8a303-199">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8a303-199">Optional.</span></span>  <br/> |
|<span data-ttu-id="8a303-200">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="8a303-200">**profileUrl**</span></span> <br/> |<span data-ttu-id="8a303-201">URL du profil de la personne qui sera utilisée comme lien hypertexte pour le nom de la personne dans l'élément de flux, si le nom de la personne est présent.</span><span class="sxs-lookup"><span data-stu-id="8a303-201">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="8a303-202">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8a303-202">Optional.</span></span>  <br/> |
|<span data-ttu-id="8a303-203">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="8a303-203">**emailAddress**</span></span> <br/> |<span data-ttu-id="8a303-204">Adresse de messagerie utilisée pour mettre à jour les informations de contact de cette personne dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="8a303-204">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="8a303-205">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8a303-205">Optional.</span></span>  <br/> |
   
### <a name="textvariable"></a><span data-ttu-id="8a303-206">textVariable</span><span class="sxs-lookup"><span data-stu-id="8a303-206">textVariable</span></span>

|<span data-ttu-id="8a303-207">**Élément**</span><span class="sxs-lookup"><span data-stu-id="8a303-207">**Element**</span></span>|<span data-ttu-id="8a303-208">**Description**</span><span class="sxs-lookup"><span data-stu-id="8a303-208">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a303-209">**nom**</span><span class="sxs-lookup"><span data-stu-id="8a303-209">**name**</span></span> <br/> |<span data-ttu-id="8a303-210">Nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="8a303-210">The name of the variable.</span></span> <span data-ttu-id="8a303-211">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8a303-211">Required.</span></span>  <br/> |
|<span data-ttu-id="8a303-212">**value**</span><span class="sxs-lookup"><span data-stu-id="8a303-212">**value**</span></span> <br/> |<span data-ttu-id="8a303-213">Texte à afficher.</span><span class="sxs-lookup"><span data-stu-id="8a303-213">The text to display.</span></span> <span data-ttu-id="8a303-214">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8a303-214">Optional.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8a303-215">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a303-215">See also</span></span>

- [<span data-ttu-id="8a303-216">Vue d'ensemble du code XML pour un élément de flux d'activité</span><span class="sxs-lookup"><span data-stu-id="8a303-216">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="8a303-217">Élément activityDetails</span><span class="sxs-lookup"><span data-stu-id="8a303-217">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="8a303-218">Élément activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="8a303-218">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="8a303-219">Instructions pour afficher correctement les activités</span><span class="sxs-lookup"><span data-stu-id="8a303-219">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="8a303-220">XML pour les activités</span><span class="sxs-lookup"><span data-stu-id="8a303-220">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="8a303-221">Schéma XML du fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="8a303-221">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="8a303-222">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="8a303-222">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

