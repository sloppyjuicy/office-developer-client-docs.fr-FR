---
title: Variables de modèle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Instances de variables de modèle (représentés par un élément templateVariable) spécifient les données d’une activité de flux d’élément dans un modèle d’activité.
ms.openlocfilehash: 99f4c2de586447fb0361e528bcd33d62b79e0fb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787729"
---
# <a name="template-variables"></a><span data-ttu-id="1b9fc-103">Variables de modèle</span><span class="sxs-lookup"><span data-stu-id="1b9fc-103">Template variables</span></span>

<span data-ttu-id="1b9fc-104">Instances de variables de modèle (représentés par un élément **templateVariable** ) spécifient les données d’une activité de flux d’élément dans un modèle d’activité.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-104">Instances of template variables (represented by a **templateVariable** element) specify the data of an activity feed item in an activity template.</span></span> 
  
<span data-ttu-id="1b9fc-105">Pour obtenir un exemple de l’activité de flux XML, voir [Exemple de code XML activité de flux](activity-feed-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="1b9fc-105">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>

<span data-ttu-id="1b9fc-106">Le tableau suivant indique les types de variables de modèle pris en charge, que chacun étant représenté par la valeur d’énumération XML correspondante.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-106">The following table shows the types of supported template variables, each represented by the corresponding XML enumeration value.</span></span>
  
|<span data-ttu-id="1b9fc-107">**Type de variable de modèle**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-107">**Type of template variable**</span></span>|<span data-ttu-id="1b9fc-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b9fc-109">**entityVariable**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-109">**entityVariable**</span></span> <br/> |<span data-ttu-id="1b9fc-110">Une personne, un groupe ou une chose.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-110">A person, group, or thing.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-111">**linkVariable**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-111">**linkVariable**</span></span> <br/> |<span data-ttu-id="1b9fc-112">Un lien.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-112">A link.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-113">**listVariable**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-113">**listVariable**</span></span> <br/> |<span data-ttu-id="1b9fc-114">Un groupe d’objets.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-114">A group of objects.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-115">**pictureVariable**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-115">**pictureVariable**</span></span> <br/> |<span data-ttu-id="1b9fc-116">Image.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-116">A picture.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-117">**publisherVariable**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-117">**publisherVariable**</span></span> <br/> |<span data-ttu-id="1b9fc-118">Élément de flux de l’éditeur de l’activité.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-118">The publisher of the activity feed item.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-119">**textVariable**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-119">**textVariable**</span></span> <br/> |<span data-ttu-id="1b9fc-120">Un bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-120">A block of text.</span></span>  <br/> |
   
<span data-ttu-id="1b9fc-121">Éléments pour spécifier les données relatives à cette variable est requis pour chaque type de variable de modèle.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-121">Each type of template variable has required elements to specify the data about that variable.</span></span> <span data-ttu-id="1b9fc-122">Variables de modèle sont spécifiés comme suit :</span><span class="sxs-lookup"><span data-stu-id="1b9fc-122">Template variables are specified as follows:</span></span>
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a><span data-ttu-id="1b9fc-123">Variable de modèle de liste</span><span class="sxs-lookup"><span data-stu-id="1b9fc-123">List template variable</span></span>

<span data-ttu-id="1b9fc-124">Vous pouvez spécifier des variables de modèle qui sont contenues dans une liste (délimitée par les éléments **listVariable** et **listItems** ) comme suit :</span><span class="sxs-lookup"><span data-stu-id="1b9fc-124">You can specify template variables that are contained within a list (delimited by the **listVariable** and **listItems** elements) as follows:</span></span> 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
<span data-ttu-id="1b9fc-125">Une variable de modèle de type **listVariable** est un conteneur pour les objets.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-125">A template variable of the **listVariable** type is a container for objects.</span></span> <span data-ttu-id="1b9fc-126">Il peut contenir les éléments délimité par des virgules (du type **linkVariable** ou **textVariable** ) ou des images (du type **pictureVariable** ).</span><span class="sxs-lookup"><span data-stu-id="1b9fc-126">It can contain comma-delimited items (of the **linkVariable** or **textVariable** type) or pictures (of the **pictureVariable** type).</span></span> <span data-ttu-id="1b9fc-127">Listes peuvent contenir jusqu'à cinq lier des éléments, cinq éléments de texte ou cinq images.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-127">Lists can contain up to five link items, five text items, or five pictures.</span></span> 
  
<span data-ttu-id="1b9fc-128">L’Outlook Social Connector (OSC) localise lien ou du texte des éléments de liste en fonction des paramètres régionaux du système de Windows.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-128">The Outlook Social Connector (OSC) localizes link or text list items according to the Windows system locale.</span></span>
  
<span data-ttu-id="1b9fc-129">Pour analyser et afficher des images dans un élément de flux d’activités correctement, vous devez inclure des images dans une liste.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-129">To correctly parse and display pictures in an activity feed item, you must include pictures in a list.</span></span> <span data-ttu-id="1b9fc-130">Toutes les images sont redimensionnés pour être 52 pixels de haut.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-130">All pictures are resized to be 52 pixels high.</span></span> <span data-ttu-id="1b9fc-131">La largeur de l’image n’est pas redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-131">The width of the picture is not resized.</span></span>
  
## <a name="template-variable-elements"></a><span data-ttu-id="1b9fc-132">Éléments de variables de modèle</span><span class="sxs-lookup"><span data-stu-id="1b9fc-132">Template variable elements</span></span>

<span data-ttu-id="1b9fc-133">Cette section décrit les éléments requis et facultatifs pris en charge pour chaque type de variable de modèle.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-133">This section covers the required and optional elements supported for each type of template variable.</span></span>
  
### <a name="entityvariable"></a><span data-ttu-id="1b9fc-134">entityVariable</span><span class="sxs-lookup"><span data-stu-id="1b9fc-134">entityVariable</span></span>

|<span data-ttu-id="1b9fc-135">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-135">**Element**</span></span>|<span data-ttu-id="1b9fc-136">**Description**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-136">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b9fc-137">**nom**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-137">**name**</span></span> <br/> |<span data-ttu-id="1b9fc-138">Le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-138">The name of the variable.</span></span> <span data-ttu-id="1b9fc-139">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-139">Required.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-140">**id**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-140">**id**</span></span> <br/> |<span data-ttu-id="1b9fc-141">ID unique de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-141">The unique ID of the user.</span></span> <span data-ttu-id="1b9fc-142">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-142">Required.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-143">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-143">**nameHint**</span></span> <br/> |<span data-ttu-id="1b9fc-144">Le nom à afficher dans l’élément de flux.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-144">The name to be displayed in the feed item.</span></span> <span data-ttu-id="1b9fc-145">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-145">Optional.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-146">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-146">**profileUrl**</span></span> <br/> |<span data-ttu-id="1b9fc-147">L’URL du profil de la personne qui sera utilisé comme le lien hypertexte pour le nom de la personne dans l’élément de flux, si le nom de personne n’est présent.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-147">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="1b9fc-148">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-148">Optional.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-149">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-149">**emailAddress**</span></span> <br/> |<span data-ttu-id="1b9fc-150">L’adresse de messagerie qui sert à mettre à jour les informations de contact de cette personne dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-150">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="1b9fc-151">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-151">Optional.</span></span>  <br/> |
   
### <a name="linkvariable"></a><span data-ttu-id="1b9fc-152">linkVariable</span><span class="sxs-lookup"><span data-stu-id="1b9fc-152">linkVariable</span></span>

|<span data-ttu-id="1b9fc-153">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-153">**Element**</span></span>|<span data-ttu-id="1b9fc-154">**Description**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b9fc-155">**nom**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-155">**name**</span></span> <br/> |<span data-ttu-id="1b9fc-156">Le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-156">The name of the variable.</span></span> <span data-ttu-id="1b9fc-157">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-157">Required.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-158">**valeur**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-158">**value**</span></span> <br/> |<span data-ttu-id="1b9fc-159">L’URL pour ce lien.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-159">The URL for this link.</span></span> <span data-ttu-id="1b9fc-160">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-160">Required.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-161">**text**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-161">**text**</span></span> <br/> |<span data-ttu-id="1b9fc-162">Le texte à afficher au lieu de l’URL du lien.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-162">The link text to display instead of the URL itself.</span></span> <span data-ttu-id="1b9fc-163">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-163">Optional.</span></span>  <br/> |
   
### <a name="listvariable"></a><span data-ttu-id="1b9fc-164">listVariable</span><span class="sxs-lookup"><span data-stu-id="1b9fc-164">listVariable</span></span>

|<span data-ttu-id="1b9fc-165">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-165">**Element**</span></span>|<span data-ttu-id="1b9fc-166">**Description**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-166">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b9fc-167">**nom**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-167">**name**</span></span> <br/> |<span data-ttu-id="1b9fc-168">Le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-168">The name of the variable.</span></span> <span data-ttu-id="1b9fc-169">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-169">Required.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-170">**listItems**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-170">**listItems**</span></span> <br/> |<span data-ttu-id="1b9fc-171">Conteneur pour les éléments dans la liste.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-171">A container for items in the list.</span></span> <span data-ttu-id="1b9fc-172">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-172">Required.</span></span>  <br/> |
   
### <a name="picturevariable"></a><span data-ttu-id="1b9fc-173">pictureVariable</span><span class="sxs-lookup"><span data-stu-id="1b9fc-173">pictureVariable</span></span>

|<span data-ttu-id="1b9fc-174">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-174">**Element**</span></span>|<span data-ttu-id="1b9fc-175">**Description**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-175">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b9fc-176">**nom**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-176">**name**</span></span> <br/> |<span data-ttu-id="1b9fc-177">Le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-177">The name of the variable.</span></span> <span data-ttu-id="1b9fc-178">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-178">Required.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-179">**valeur**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-179">**value**</span></span> <br/> |<span data-ttu-id="1b9fc-180">L’URL de l’image.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-180">The URL for the picture.</span></span> <span data-ttu-id="1b9fc-181">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-181">Required.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-182">**altText**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-182">**altText**</span></span> <br/> |<span data-ttu-id="1b9fc-183">Le texte de remplacement à afficher pour l’accessibilité et lorsque l’utilisateur déplace le pointeur de la souris sur l’image.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-183">The alternate text to display for accessibility and when the user moves the mouse pointer over the picture.</span></span> <span data-ttu-id="1b9fc-184">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-184">Optional.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-185">**href**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-185">**href**</span></span> <br/> |<span data-ttu-id="1b9fc-186">Le lien hypertexte à utiliser lorsque l’utilisateur clique sur l’image, si la cible souhaitée n’est pas l’URL de l’image spécifiée par l’élément de **valeur** .</span><span class="sxs-lookup"><span data-stu-id="1b9fc-186">The hyperlink to use when the user clicks the picture, if the desired target is not the picture URL specified by the **value** element.</span></span> <span data-ttu-id="1b9fc-187">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-187">Optional.</span></span>  <br/> |
   
### <a name="publishervariable"></a><span data-ttu-id="1b9fc-188">publisherVariable</span><span class="sxs-lookup"><span data-stu-id="1b9fc-188">publisherVariable</span></span>

|<span data-ttu-id="1b9fc-189">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-189">**Element**</span></span>|<span data-ttu-id="1b9fc-190">**Description**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-190">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b9fc-191">**nom**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-191">**name**</span></span> <br/> |<span data-ttu-id="1b9fc-192">Le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-192">The name of the variable.</span></span> <span data-ttu-id="1b9fc-193">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-193">Required.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-194">**id**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-194">**id**</span></span> <br/> |<span data-ttu-id="1b9fc-195">ID unique de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-195">The unique ID of the user.</span></span> <span data-ttu-id="1b9fc-196">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-196">Required.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-197">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-197">**nameHint**</span></span> <br/> |<span data-ttu-id="1b9fc-198">Le nom à afficher dans l’élément de flux.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-198">The name to be displayed in the feed item.</span></span> <span data-ttu-id="1b9fc-199">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-199">Optional.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-200">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-200">**profileUrl**</span></span> <br/> |<span data-ttu-id="1b9fc-201">L’URL du profil de la personne qui sera utilisé comme le lien hypertexte pour le nom de la personne dans l’élément de flux, si le nom de personne n’est présent.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-201">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="1b9fc-202">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-202">Optional.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-203">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-203">**emailAddress**</span></span> <br/> |<span data-ttu-id="1b9fc-204">L’adresse de messagerie qui sert à mettre à jour les informations de contact de cette personne dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-204">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="1b9fc-205">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-205">Optional.</span></span>  <br/> |
   
### <a name="textvariable"></a><span data-ttu-id="1b9fc-206">textVariable</span><span class="sxs-lookup"><span data-stu-id="1b9fc-206">textVariable</span></span>

|<span data-ttu-id="1b9fc-207">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-207">**Element**</span></span>|<span data-ttu-id="1b9fc-208">**Description**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-208">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b9fc-209">**nom**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-209">**name**</span></span> <br/> |<span data-ttu-id="1b9fc-210">Le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-210">The name of the variable.</span></span> <span data-ttu-id="1b9fc-211">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-211">Required.</span></span>  <br/> |
|<span data-ttu-id="1b9fc-212">**valeur**</span><span class="sxs-lookup"><span data-stu-id="1b9fc-212">**value**</span></span> <br/> |<span data-ttu-id="1b9fc-213">Le texte à afficher.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-213">The text to display.</span></span> <span data-ttu-id="1b9fc-214">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="1b9fc-214">Optional.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1b9fc-215">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b9fc-215">See also</span></span>

- [<span data-ttu-id="1b9fc-216">Vue d’ensemble du code XML pour une activité de flux d’élément</span><span class="sxs-lookup"><span data-stu-id="1b9fc-216">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="1b9fc-217">activityDetails, élément</span><span class="sxs-lookup"><span data-stu-id="1b9fc-217">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="1b9fc-218">activityTemplateContainer, élément</span><span class="sxs-lookup"><span data-stu-id="1b9fc-218">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="1b9fc-219">Conseils pour l’affichage correctement les activités</span><span class="sxs-lookup"><span data-stu-id="1b9fc-219">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="1b9fc-220">XML pour les activités</span><span class="sxs-lookup"><span data-stu-id="1b9fc-220">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="1b9fc-221">Fournisseur Outlook Social Connector schéma XML</span><span class="sxs-lookup"><span data-stu-id="1b9fc-221">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="1b9fc-222">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="1b9fc-222">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

