---
title: Flux de saisie semi-automatique
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8b5c5fee71db0fc7bdd6e01c58e9c9a9c3d9fa22
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318080"
---
# <a name="autocomplete-stream"></a><span data-ttu-id="d125e-103">Flux de saisie semi-automatique</span><span class="sxs-lookup"><span data-stu-id="d125e-103">Autocomplete Stream</span></span>

  
  
<span data-ttu-id="d125e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d125e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d125e-105">Outre le fait de savoir comment Microsoft Outlook interagit avec le flux de saisie semi-automatique, vous devez également comprendre le format binaire du flux de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="d125e-105">In addition to knowing how Microsoft Outlook interacts with the autocomplete stream, you must also understand the binary format of the autocomplete stream.</span></span>
  
<span data-ttu-id="d125e-106">Le flux de saisie semi-automatique est un ensemble de lignes de propriété de destinataire qui sont enregistrés sous la forme d’un flux binaire avec certaines métadonnées comptables, utilisées uniquement par Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007 et Microsoft Outlook 2003.</span><span class="sxs-lookup"><span data-stu-id="d125e-106">The autocomplete stream is a set of recipient property rows that are saved as a binary stream together with some bookkeeping metadata that is used only by Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007, and Microsoft Outlook 2003.</span></span> <span data-ttu-id="d125e-107">Les métadonnées sont pertinentes pour les interactions Outlook avec le flux de saisie semi-automatique afin que les tiers conservent ce qui se trouve dans chaque bloc de métadonnées lorsqu’ils enregistrent un flux de saisie semi-automatique modifié.</span><span class="sxs-lookup"><span data-stu-id="d125e-107">The metadata is relevant to Outlook interactions with the autocomplete stream so third parties must preserve what is in each metadata block when they save a modified autocomplete stream.</span></span> <span data-ttu-id="d125e-108">En d’autres termes, les tiers doivent modifier uniquement la partie de ligne la plus riche du format binaire et conserver ce qui était déjà dans les blocs de métadonnées du flux de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="d125e-108">In other words, third parties should modify only the row-set part of the binary format and preserve what was already in the metadata blocks of the autocomplete stream.</span></span>
  
## <a name="stream-visualization"></a><span data-ttu-id="d125e-109">Visualisation de flux de données</span><span class="sxs-lookup"><span data-stu-id="d125e-109">Stream Visualization</span></span>

<span data-ttu-id="d125e-110">La mise en page générale du flux de saisie semi-automatique est comme suit :</span><span class="sxs-lookup"><span data-stu-id="d125e-110">The high-level layout of the autocomplete stream is as follows:</span></span>
  
<span data-ttu-id="d125e-111">Métadonnées (4 octets)</span><span class="sxs-lookup"><span data-stu-id="d125e-111">Metadata (4 bytes)</span></span>
  
<span data-ttu-id="d125e-112">Numéro de version majeure (4 octets)</span><span class="sxs-lookup"><span data-stu-id="d125e-112">Major Version Number (4 bytes)</span></span>
  
<span data-ttu-id="d125e-113">Numéro de version mineure (4 octets)</span><span class="sxs-lookup"><span data-stu-id="d125e-113">Minor Version Number (4 bytes)</span></span>
  
<span data-ttu-id="d125e-114">Nombre n de lignes (4 octets)</span><span class="sxs-lookup"><span data-stu-id="d125e-114">Number of rows n (4 bytes)</span></span>
  
<span data-ttu-id="d125e-115">Nombre de propriétés p dans la ligne une (4 octets)</span><span class="sxs-lookup"><span data-stu-id="d125e-115">Number of properties p in row one (4 bytes)</span></span>
  
<span data-ttu-id="d125e-116">Balise de propriété de la propriété 1 (4 octets)</span><span class="sxs-lookup"><span data-stu-id="d125e-116">Property 1's property tag (4 bytes)</span></span>
  
<span data-ttu-id="d125e-117">Données réservées de la propriété 1 (4 octets)</span><span class="sxs-lookup"><span data-stu-id="d125e-117">Property 1's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="d125e-118">Union de valeur de la propriété 1 (8 octets)</span><span class="sxs-lookup"><span data-stu-id="d125e-118">Property 1's value union (8 bytes)</span></span>
  
<span data-ttu-id="d125e-119">Données de valeur de la propriété 1 (0 octet ou octets variables)</span><span class="sxs-lookup"><span data-stu-id="d125e-119">Property 1's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="d125e-120">…</span><span class="sxs-lookup"><span data-stu-id="d125e-120"></span></span> <span data-ttu-id="d125e-121">(propriété 2 via propriété P-1)</span><span class="sxs-lookup"><span data-stu-id="d125e-121">(property 2 through property P-1)</span></span>
  
<span data-ttu-id="d125e-122">Balise de propriété de la propriété p (4 octets)</span><span class="sxs-lookup"><span data-stu-id="d125e-122">Property p's property tag (4 bytes)</span></span>
  
<span data-ttu-id="d125e-123">Données réservées de la propriété p (4 octets)</span><span class="sxs-lookup"><span data-stu-id="d125e-123">Property p's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="d125e-124">Union de valeur de la propriété p (8 octets)</span><span class="sxs-lookup"><span data-stu-id="d125e-124">Property p's value union (8 bytes)</span></span>
  
<span data-ttu-id="d125e-125">Données de valeur de la propriété p (0 octet ou octets variables)</span><span class="sxs-lookup"><span data-stu-id="d125e-125">Property p's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="d125e-126">Nombre de propriétés q dans la ligne deux (4 octets)</span><span class="sxs-lookup"><span data-stu-id="d125e-126">Number of properties q in row two (4 bytes)</span></span>
  
<span data-ttu-id="d125e-127">…</span><span class="sxs-lookup"><span data-stu-id="d125e-127"></span></span> <span data-ttu-id="d125e-128">(propriétés de la ligne deux)</span><span class="sxs-lookup"><span data-stu-id="d125e-128">(row two's properties)</span></span>
  
<span data-ttu-id="d125e-129">…</span><span class="sxs-lookup"><span data-stu-id="d125e-129"></span></span> <span data-ttu-id="d125e-130">(ligne 3 via ligne n-1)</span><span class="sxs-lookup"><span data-stu-id="d125e-130">(row 3 through row n-1)</span></span>
  
<span data-ttu-id="d125e-131">Nombre de propriétés r dans la ligne n (4 octets)</span><span class="sxs-lookup"><span data-stu-id="d125e-131">Number of properties r in row n (4 bytes)</span></span>
  
<span data-ttu-id="d125e-132">…</span><span class="sxs-lookup"><span data-stu-id="d125e-132"></span></span> <span data-ttu-id="d125e-133">(propriétés de la ligne n)</span><span class="sxs-lookup"><span data-stu-id="d125e-133">(row n's properties)</span></span>
  
<span data-ttu-id="d125e-134">Nombre d’octets des infos supplémentaires EI (4 octets)</span><span class="sxs-lookup"><span data-stu-id="d125e-134">Extra information byte count EI (4 bytes)</span></span>
  
<span data-ttu-id="d125e-135">Infos supplémentaires (octets EI)</span><span class="sxs-lookup"><span data-stu-id="d125e-135">Extra information (EI bytes)</span></span>
  
<span data-ttu-id="d125e-136">Métadonnées (8 octets)</span><span class="sxs-lookup"><span data-stu-id="d125e-136">Metadata (8 bytes)</span></span>
  
<span data-ttu-id="d125e-137">Pour un exemple de structure binaire, reportez-vous à la section Exemple binaire dans [Consignes pour le développement et le format de fichier NK2 Outlook 2003/2007](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf).</span><span class="sxs-lookup"><span data-stu-id="d125e-137">For an example of a binary structure, see Binary Example in the [Outlook 2003/2007 NK2 File Format and Developer Guidelines.](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span></span>
  
## <a name="high-level-layout"></a><span data-ttu-id="d125e-138">Mise en page générale</span><span class="sxs-lookup"><span data-stu-id="d125e-138">High-level Layout</span></span>

<span data-ttu-id="d125e-139">De manière générale, la mise en page du flux de saisie semi-automatique est comme suit :</span><span class="sxs-lookup"><span data-stu-id="d125e-139">Broadly speaking, the layout of the autocomplete stream is as follows:</span></span>
  
|<span data-ttu-id="d125e-140">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="d125e-140">**Value Data**</span></span>|<span data-ttu-id="d125e-141">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="d125e-141">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d125e-142">Métadonnées</span><span class="sxs-lookup"><span data-stu-id="d125e-142">Metadata</span></span>  <br/> |<span data-ttu-id="d125e-143">4</span><span class="sxs-lookup"><span data-stu-id="d125e-143">4</span></span>  <br/> |
|<span data-ttu-id="d125e-144">Numéro de version majeure</span><span class="sxs-lookup"><span data-stu-id="d125e-144">Major Version Number</span></span>  <br/> |<span data-ttu-id="d125e-145">4</span><span class="sxs-lookup"><span data-stu-id="d125e-145">4</span></span>  <br/> |
|<span data-ttu-id="d125e-146">Numéro de version mineure</span><span class="sxs-lookup"><span data-stu-id="d125e-146">Minor Version Number</span></span>  <br/> |<span data-ttu-id="d125e-147">4</span><span class="sxs-lookup"><span data-stu-id="d125e-147">4</span></span>  <br/> |
|<span data-ttu-id="d125e-148">Ensemble de lignes</span><span class="sxs-lookup"><span data-stu-id="d125e-148">Row-set</span></span>  <br/> |<span data-ttu-id="d125e-149">Variable</span><span class="sxs-lookup"><span data-stu-id="d125e-149">Variable</span></span>  <br/> |
|<span data-ttu-id="d125e-150">Nombre d’octets des infos supplémentaires EI</span><span class="sxs-lookup"><span data-stu-id="d125e-150">Extra information byte count EI</span></span>  <br/> |<span data-ttu-id="d125e-151">4</span><span class="sxs-lookup"><span data-stu-id="d125e-151">4</span></span>  <br/> |
|<span data-ttu-id="d125e-152">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="d125e-152">Extra information</span></span>  <br/> |<span data-ttu-id="d125e-153">EI </span><span class="sxs-lookup"><span data-stu-id="d125e-153">EI</span></span>  <br/> |
|<span data-ttu-id="d125e-154">Métadonnées</span><span class="sxs-lookup"><span data-stu-id="d125e-154">Metadata</span></span>  <br/> |<span data-ttu-id="d125e-155">8bits</span><span class="sxs-lookup"><span data-stu-id="d125e-155">8</span></span>  <br/> |
   
<span data-ttu-id="d125e-156">Lors de la lecture de ce flux, si la version majeure n’est pas la 12, alors ce flux de données ne doit pas être lu ou écrit.</span><span class="sxs-lookup"><span data-stu-id="d125e-156">When reading this stream, if the major version is different than 12, then this stream should not be read or written.</span></span> <span data-ttu-id="d125e-157">La version mineure actuelle du flux de saisie semi-automatique est la 0, pour laquelle le nombre d’octets d’informations supplémentaire est égal à 0.</span><span class="sxs-lookup"><span data-stu-id="d125e-157">The current minor version of the autocomplete stream is 0, which has the Extra Information Byte count set to 0.</span></span> <span data-ttu-id="d125e-158">Si la version mineure est différente de 0, il y aura alors des informations supplémentaires qui doivent être lues lors de la lecture du flux de données et conservées lors de la rédaction du flux d’informations.</span><span class="sxs-lookup"><span data-stu-id="d125e-158">If the minor version is different than 0, then there will be information in the extra information that needs to be read when reading the stream and preserved when writing the stream.</span></span> <span data-ttu-id="d125e-159">La version mineure doit également être conservée lors de la rédaction du flux de données.</span><span class="sxs-lookup"><span data-stu-id="d125e-159">The minor version will also need to be preserved when writing the stream.</span></span> <span data-ttu-id="d125e-160">Si ces deux éléments ne sont pas conservés, les instances d’Outlook écrites par les informations supplémentaires perdent des données.</span><span class="sxs-lookup"><span data-stu-id="d125e-160">If both of these are not preserved, instances of Outlook that wrote the extra information will lose data.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d125e-161">Les applications ne doivent pas ajouter de données personnalisées au champ Informations supplémentaires ni changer la version mineure, car cette fonctionnalité doit prendre en charge les extensions Outlook au format et non des extensions tiers arbitraires.</span><span class="sxs-lookup"><span data-stu-id="d125e-161">Applications must not add custom data to the Extra Information field or change the minor version as this functionality is to support Outlook extensions to the format and not arbitrary third-party extensions.</span></span> 
  
## <a name="row-set-layout"></a><span data-ttu-id="d125e-162">Disposition de jeu de lignes</span><span class="sxs-lookup"><span data-stu-id="d125e-162">Row-set Layout</span></span>

<span data-ttu-id="d125e-163">La disposition de jeu de lignes est comme suit :</span><span class="sxs-lookup"><span data-stu-id="d125e-163">The row-set layout is as follows:</span></span> 
  
|<span data-ttu-id="d125e-164">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="d125e-164">**Value Data**</span></span>|<span data-ttu-id="d125e-165">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="d125e-165">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d125e-166">Nombre de lignes</span><span class="sxs-lookup"><span data-stu-id="d125e-166">Number of rows</span></span>  <br/> |<span data-ttu-id="d125e-167">4</span><span class="sxs-lookup"><span data-stu-id="d125e-167">4</span></span>  <br/> |
|<span data-ttu-id="d125e-168">Lignes</span><span class="sxs-lookup"><span data-stu-id="d125e-168">Rows</span></span>  <br/> |<span data-ttu-id="d125e-169">Variable</span><span class="sxs-lookup"><span data-stu-id="d125e-169">Variable</span></span>  <br/> |
   
<span data-ttu-id="d125e-170">Le nombre de lignes identifie le nombre de lignes fournies dans la partie suivante de la séquence de flux binaire.</span><span class="sxs-lookup"><span data-stu-id="d125e-170">The number of rows identifies how many rows come in the next part of the binary stream sequence.</span></span>
  
## <a name="row-layout"></a><span data-ttu-id="d125e-171">Disposition de ligne</span><span class="sxs-lookup"><span data-stu-id="d125e-171">Row Layout</span></span>

<span data-ttu-id="d125e-172">Chaque ligne correspond au format suivant :</span><span class="sxs-lookup"><span data-stu-id="d125e-172">Each row is of the following format:</span></span>
  
|<span data-ttu-id="d125e-173">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="d125e-173">**Value Data**</span></span>|<span data-ttu-id="d125e-174">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="d125e-174">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d125e-175">Nombre de propriétés</span><span class="sxs-lookup"><span data-stu-id="d125e-175">Number of properties</span></span>  <br/> |<span data-ttu-id="d125e-176">4</span><span class="sxs-lookup"><span data-stu-id="d125e-176">4</span></span>  <br/> |
|<span data-ttu-id="d125e-177">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d125e-177">Properties</span></span>  <br/> |<span data-ttu-id="d125e-178">Variable</span><span class="sxs-lookup"><span data-stu-id="d125e-178">Variable</span></span>  <br/> |
   
<span data-ttu-id="d125e-179">Le nombre de lignes identifie le nombre de propriétés fournies dans la partie suivante de la séquence de flux binaire.</span><span class="sxs-lookup"><span data-stu-id="d125e-179">The number of properties identifies how many properties come in the next part of the binary stream sequence.</span></span>
  
## <a name="property-layout"></a><span data-ttu-id="d125e-180">Disposition de propriété</span><span class="sxs-lookup"><span data-stu-id="d125e-180">Property Layout</span></span>

<span data-ttu-id="d125e-181">Chaque propriété correspond au format suivant :</span><span class="sxs-lookup"><span data-stu-id="d125e-181">Each property is of the following format:</span></span>
  
|<span data-ttu-id="d125e-182">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="d125e-182">**Value Data**</span></span>|<span data-ttu-id="d125e-183">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="d125e-183">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d125e-184">Balise de propriété</span><span class="sxs-lookup"><span data-stu-id="d125e-184">Property Tag</span></span>  <br/> |<span data-ttu-id="d125e-185">4</span><span class="sxs-lookup"><span data-stu-id="d125e-185">4</span></span>  <br/> |
|<span data-ttu-id="d125e-186">Données réservées</span><span class="sxs-lookup"><span data-stu-id="d125e-186">Reserved Data</span></span>  <br/> |<span data-ttu-id="d125e-187">4</span><span class="sxs-lookup"><span data-stu-id="d125e-187">4</span></span>  <br/> |
|<span data-ttu-id="d125e-188">Union de valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d125e-188">Property Value Union</span></span>  <br/> ||
|<span data-ttu-id="d125e-189">Données de la valeur</span><span class="sxs-lookup"><span data-stu-id="d125e-189">Value Data</span></span>  <br/> |<span data-ttu-id="d125e-190">0 ou variable (en fonction de la balise de proposition)</span><span class="sxs-lookup"><span data-stu-id="d125e-190">0 or variable (depending on the prop tag)</span></span>  <br/> |
   
## <a name="interpreting-the-property-value"></a><span data-ttu-id="d125e-191">Interprétation de la valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="d125e-191">Interpreting the Property Value</span></span>

<span data-ttu-id="d125e-192">L’union de valeur de propriété et les données de valeur doivent être interprétées en fonction de la balise de propriété dans les 4 octets du bloc de propriété.</span><span class="sxs-lookup"><span data-stu-id="d125e-192">The Property Value Union and the Value Data are to be interpreted based on the property tag in the first 4 bytes of the property block.</span></span> <span data-ttu-id="d125e-193">Cette balise de propriété a le même format qu’une balise de propriété MAPI.</span><span class="sxs-lookup"><span data-stu-id="d125e-193">This property tag is in the same format as a MAPI property tag.</span></span> <span data-ttu-id="d125e-194">Les bits 0 à 15 de l’indicateur de propriété correspondent au type de propriété.</span><span class="sxs-lookup"><span data-stu-id="d125e-194">Bits 0 through 15 of the property tag are the property's type.</span></span> <span data-ttu-id="d125e-195">Les bits 16 à 31 correspondent à l’identificateur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="d125e-195">Bits 16 through 31 are the property's identifier.</span></span> <span data-ttu-id="d125e-196">Le type de propriété détermine comment le reste de la propriété doit être lu.</span><span class="sxs-lookup"><span data-stu-id="d125e-196">The property type determines how the rest of the property should be read.</span></span>
  
## <a name="static-value"></a><span data-ttu-id="d125e-197">Valeur statique</span><span class="sxs-lookup"><span data-stu-id="d125e-197">Static Value</span></span>

<span data-ttu-id="d125e-198">Certaines propriétés ne possèdent aucune valeur de données et ont uniquement des données dans l’union.</span><span class="sxs-lookup"><span data-stu-id="d125e-198">Some properties have no Value Data and only have data in the union.</span></span> <span data-ttu-id="d125e-199">Les types de propriété suivants (qui proviennent de la balise de propriété) doivent interpréter les Union de données de propriété à 8 octets comme suit :</span><span class="sxs-lookup"><span data-stu-id="d125e-199">The following property types (which come from the Property Tag) should interpret the 8-byte Property Union data as follows:</span></span>
  
|<span data-ttu-id="d125e-200">**Type de proposition**</span><span class="sxs-lookup"><span data-stu-id="d125e-200">**Prop Type**</span></span>|<span data-ttu-id="d125e-201">**Interprétation de l’union de propriété**</span><span class="sxs-lookup"><span data-stu-id="d125e-201">**Property Union Interpretation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d125e-202">PT_I2</span><span class="sxs-lookup"><span data-stu-id="d125e-202">PT_I2</span></span>  <br/> |<span data-ttu-id="d125e-203">short int</span><span class="sxs-lookup"><span data-stu-id="d125e-203">short int</span></span>  <br/> |
|<span data-ttu-id="d125e-204">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d125e-204">PT_LONG</span></span>  <br/> |<span data-ttu-id="d125e-205">long</span><span class="sxs-lookup"><span data-stu-id="d125e-205">long</span></span>  <br/> |
|<span data-ttu-id="d125e-206">PT_R4</span><span class="sxs-lookup"><span data-stu-id="d125e-206">PT_R4</span></span>  <br/> |<span data-ttu-id="d125e-207">float</span><span class="sxs-lookup"><span data-stu-id="d125e-207">float</span></span>  <br/> |
|<span data-ttu-id="d125e-208">PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="d125e-208">PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="d125e-209">double</span><span class="sxs-lookup"><span data-stu-id="d125e-209">double</span></span>  <br/> |
|<span data-ttu-id="d125e-210">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d125e-210">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="d125e-211">short int</span><span class="sxs-lookup"><span data-stu-id="d125e-211">short int</span></span>  <br/> |
|<span data-ttu-id="d125e-212">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d125e-212">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="d125e-213">FILETIME</span><span class="sxs-lookup"><span data-stu-id="d125e-213">FILETIME</span></span>  <br/> |
|<span data-ttu-id="d125e-214">PT_I8</span><span class="sxs-lookup"><span data-stu-id="d125e-214">PT_I8</span></span>  <br/> |<span data-ttu-id="d125e-215">LARGE_INTEGER</span><span class="sxs-lookup"><span data-stu-id="d125e-215">LARGE_INTEGER</span></span>  <br/> |
   
## <a name="dynamic-values"></a><span data-ttu-id="d125e-216">Valeurs dynamiques</span><span class="sxs-lookup"><span data-stu-id="d125e-216">Dynamic Values</span></span>

<span data-ttu-id="d125e-217">Les autres propriétés possèdent des données dans un bloc de données de la valeur après que les 16 premiers octets contiennent la balise de propriété, les données réservées et l’union de valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="d125e-217">Other properties have data in a Value Data block after the first 16 bytes that contain the Property Tag, the Reserved Data, and the Property Value Union.</span></span> <span data-ttu-id="d125e-218">Contrairement aux valeurs statiques, les données stockées dans l’union de valeur de propriété de 8 octets ne sont pas pertinentes à la lecture.</span><span class="sxs-lookup"><span data-stu-id="d125e-218">Unlike static values, the data that is stored in the 8-byte Property Value union is irrelevant on reading.</span></span> <span data-ttu-id="d125e-219">Lorsque vous rédigez, assurez-vous que vous complétez correctement ces 8 octets.</span><span class="sxs-lookup"><span data-stu-id="d125e-219">When writing, make sure that you fill these 8 bytes with something.</span></span> <span data-ttu-id="d125e-220">Toutefois, le contenu des 8 octets n’est pas important.</span><span class="sxs-lookup"><span data-stu-id="d125e-220">However, the content of the 8 bytes is not important.</span></span> <span data-ttu-id="d125e-221">Dans les valeurs dynamiques, le type de la balise de propriété détermine la manière d’interpréter les données de valeur.</span><span class="sxs-lookup"><span data-stu-id="d125e-221">In dynamic values, the property tag's type determines how to interpret the Value Data.</span></span>
  
<span data-ttu-id="d125e-222">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="d125e-222">PT_STRING8</span></span> 
  
|<span data-ttu-id="d125e-223">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="d125e-223">**Value Data**</span></span>|<span data-ttu-id="d125e-224">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="d125e-224">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d125e-225">Nombre d’octets n</span><span class="sxs-lookup"><span data-stu-id="d125e-225">Number of bytes n</span></span>  <br/> |<span data-ttu-id="d125e-226">4</span><span class="sxs-lookup"><span data-stu-id="d125e-226">4</span></span>  <br/> |
|<span data-ttu-id="d125e-227">Les octets seront interprétés comme une chaîne ANSI (y compris terminateur NULL)</span><span class="sxs-lookup"><span data-stu-id="d125e-227">Bytes to be interpreted as an ANSI string (includes NULL terminator)</span></span>  <br/> |<span data-ttu-id="d125e-228">n</span><span class="sxs-lookup"><span data-stu-id="d125e-228">n</span></span>  <br/> |
   
<span data-ttu-id="d125e-229">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="d125e-229">PT_CLSID</span></span>
  
|<span data-ttu-id="d125e-230">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="d125e-230">**Value Data**</span></span>|<span data-ttu-id="d125e-231">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="d125e-231">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d125e-232">Les octets seront interprétés comme un GUID</span><span class="sxs-lookup"><span data-stu-id="d125e-232">Bytes to be interpreted as a GUID</span></span>  <br/> |<span data-ttu-id="d125e-233">Seiz</span><span class="sxs-lookup"><span data-stu-id="d125e-233">16</span></span>  <br/> |
|||
   
<span data-ttu-id="d125e-234">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d125e-234">PT_BINARY</span></span> 
  
|<span data-ttu-id="d125e-235">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="d125e-235">**Value Data**</span></span>|<span data-ttu-id="d125e-236">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="d125e-236">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d125e-237">Nombre d’octets n</span><span class="sxs-lookup"><span data-stu-id="d125e-237">Number of bytes n</span></span>  <br/> |<span data-ttu-id="d125e-238">4</span><span class="sxs-lookup"><span data-stu-id="d125e-238">4</span></span>  <br/> |
|<span data-ttu-id="d125e-239">Les octets seront interprétés comme une gamme d’octets</span><span class="sxs-lookup"><span data-stu-id="d125e-239">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="d125e-240">n</span><span class="sxs-lookup"><span data-stu-id="d125e-240">n</span></span>  <br/> |
   
<span data-ttu-id="d125e-241">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="d125e-241">PT_ERROR</span></span>
  
|<span data-ttu-id="d125e-242">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="d125e-242">**Value Data**</span></span>|<span data-ttu-id="d125e-243">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="d125e-243">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d125e-244">Nombre d’octets n</span><span class="sxs-lookup"><span data-stu-id="d125e-244">Number of bytes n</span></span>  <br/> |<span data-ttu-id="d125e-245">4</span><span class="sxs-lookup"><span data-stu-id="d125e-245">4</span></span>  <br/> |
|<span data-ttu-id="d125e-246">Les octets seront interprétés comme une gamme d’octets</span><span class="sxs-lookup"><span data-stu-id="d125e-246">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="d125e-247">n</span><span class="sxs-lookup"><span data-stu-id="d125e-247">n</span></span>  <br/> |
   
<span data-ttu-id="d125e-248">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="d125e-248">PT_MV_BINARY</span></span>
  
|<span data-ttu-id="d125e-249">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="d125e-249">**Value Data**</span></span>|<span data-ttu-id="d125e-250">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="d125e-250">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d125e-251">Nombre de matrices binaires X</span><span class="sxs-lookup"><span data-stu-id="d125e-251">Number of binary arrays X</span></span>  <br/> |<span data-ttu-id="d125e-252">4</span><span class="sxs-lookup"><span data-stu-id="d125e-252">4</span></span>  <br/> |
|<span data-ttu-id="d125e-253">Une exécution d’octets contenant X matrices binaires.</span><span class="sxs-lookup"><span data-stu-id="d125e-253">A run of bytes that contains X binary arrays.</span></span> <span data-ttu-id="d125e-254">Chaque tableau doit être interprété exactement comme l’exécution d’octet PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="d125e-254">Each array should be interpreted exactly like the PT_BINARY byte run.</span></span>  <br/> |<span data-ttu-id="d125e-255">Variable</span><span class="sxs-lookup"><span data-stu-id="d125e-255">Variable</span></span>  <br/> |
   
<span data-ttu-id="d125e-256">PT_MV_STRING8 (Outlook 2007, Outlook 2010, et Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="d125e-256">PT_MV_STRING8 (Outlook 2007, Outlook 2010, and Outlook 2013)</span></span>
  
|<span data-ttu-id="d125e-257">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="d125e-257">**Value Data**</span></span>|<span data-ttu-id="d125e-258">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="d125e-258">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d125e-259">Nombre de chaînes ANSI X</span><span class="sxs-lookup"><span data-stu-id="d125e-259">Number of ANSI strings X</span></span>  <br/> |<span data-ttu-id="d125e-260">4</span><span class="sxs-lookup"><span data-stu-id="d125e-260">4</span></span>  <br/> |
|<span data-ttu-id="d125e-261">Une exécution d’octets contenant X chaînes ANSI.</span><span class="sxs-lookup"><span data-stu-id="d125e-261">A run of bytes that contains X ANSI strings.</span></span> <span data-ttu-id="d125e-262">Chaque tableau doit être interprété exactement comme l’exécution d’octets PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="d125e-262">Each string should be interpreted exactly like the PT_STRING8 byte run.</span></span>  <br/> |<span data-ttu-id="d125e-263">Variable</span><span class="sxs-lookup"><span data-stu-id="d125e-263">Variable</span></span>  <br/> |
   
<span data-ttu-id="d125e-264">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="d125e-264">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span></span>
  
|<span data-ttu-id="d125e-265">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="d125e-265">**Value Data**</span></span>|<span data-ttu-id="d125e-266">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="d125e-266">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d125e-267">Nombre de chaînes UNICODE X</span><span class="sxs-lookup"><span data-stu-id="d125e-267">Number of UNICODE strings X</span></span>  <br/> |<span data-ttu-id="d125e-268">4</span><span class="sxs-lookup"><span data-stu-id="d125e-268">4</span></span>  <br/> |
|<span data-ttu-id="d125e-269">Une exécution d’octets contenant X chaînes UNICODE.</span><span class="sxs-lookup"><span data-stu-id="d125e-269">A run of bytes that contains X UNICODE strings.</span></span> <span data-ttu-id="d125e-270">Chaque tableau doit être interprété exactement comme l’exécution d’octets PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="d125e-270">Each string should be interpreted exactly like the PT_UNICODE byte run.</span></span>  <br/> |<span data-ttu-id="d125e-271">Variable</span><span class="sxs-lookup"><span data-stu-id="d125e-271">Variable</span></span>  <br/> |
   
## <a name="significant-properties"></a><span data-ttu-id="d125e-272">Propriétés importantes</span><span class="sxs-lookup"><span data-stu-id="d125e-272">Significant properties</span></span>

<span data-ttu-id="d125e-273">Comme mentionné précédemment dans cette rubrique, les blocs binaires qui représentent les propriétés possèdent des balises de propriété correspondant aux propriétés destinataires du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="d125e-273">As mentioned previously in this topic, the binary blocks that represent properties have property tags that correspond to properties on address book recipients.</span></span> <span data-ttu-id="d125e-274">Pour les propriétés qui ne sont pas répertoriées ici, vous pouvez consulter la description de la propriété àhttps://msdn.microsoft.com/library/cc433490(EXCHG.80).aspx.</span><span class="sxs-lookup"><span data-stu-id="d125e-274">For properties that are not listed here, you can look up the property description at https://msdn.microsoft.com/library/cc433490(EXCHG.80).aspx.</span></span>
  
|<span data-ttu-id="d125e-275">**Nom de la propriété**</span><span class="sxs-lookup"><span data-stu-id="d125e-275">**Property Name**</span></span>|<span data-ttu-id="d125e-276">**Balise de propriété**</span><span class="sxs-lookup"><span data-stu-id="d125e-276">**Property Tag**</span></span>|<span data-ttu-id="d125e-277">**Description (pour plus d’informations, consultez MSDN)**</span><span class="sxs-lookup"><span data-stu-id="d125e-277">**Description (see MSDN for more information)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d125e-278">PR_NICK_NAME_W (non transmis aux destinataires, spécifiques uniquement aux flux de saisie semi-automatique)</span><span class="sxs-lookup"><span data-stu-id="d125e-278">PR_NICK_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="d125e-279">0x6001001f</span><span class="sxs-lookup"><span data-stu-id="d125e-279">0x6001001f</span></span>  <br/> |<span data-ttu-id="d125e-280">Cette propriété doit être la première dans chaque ligne du destinataire.</span><span class="sxs-lookup"><span data-stu-id="d125e-280">This property must be first in each recipient row.</span></span> <span data-ttu-id="d125e-281">Sur le plan opérationnel, elle correspond à un identificateur de clé pour la ligne du destinataire.</span><span class="sxs-lookup"><span data-stu-id="d125e-281">It functionally serves as a key identifier for the recipient row.</span></span>  <br/> |
|<span data-ttu-id="d125e-282">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d125e-282">PR_ENTRYID</span></span>  <br/> |<span data-ttu-id="d125e-283">0x0FFF0102</span><span class="sxs-lookup"><span data-stu-id="d125e-283">0x0FFF0102</span></span>  <br/> |<span data-ttu-id="d125e-284">L’identificateur d’entrée Carnet d’adresses du destinataire.</span><span class="sxs-lookup"><span data-stu-id="d125e-284">The address book entry identifier for the recipient.</span></span>  <br/> |
|<span data-ttu-id="d125e-285">PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="d125e-285">PR_DISPLAY_NAME_W</span></span>  <br/> |<span data-ttu-id="d125e-286">0x3001001F</span><span class="sxs-lookup"><span data-stu-id="d125e-286">0x3001001F</span></span>  <br/> |<span data-ttu-id="d125e-287">Le nom d’affichage du destinataire.</span><span class="sxs-lookup"><span data-stu-id="d125e-287">The recipient's display name.</span></span>  <br/> |
|<span data-ttu-id="d125e-288">PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="d125e-288">PR_EMAIL_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="d125e-289">0x3003001F</span><span class="sxs-lookup"><span data-stu-id="d125e-289">0x3003001F</span></span>  <br/> |<span data-ttu-id="d125e-290">Adresse de courrier du destinataire (par exemple, johndoe@contoso.com ou /o=Contoso/OU=Foo/cn=Destintaires/cn=Durand)</span><span class="sxs-lookup"><span data-stu-id="d125e-290">The recipient's email address (e.g. johndoe@contoso.com or /o=Contoso/OU=Foo/cn=Recipients/cn=johndoe)</span></span>  <br/> |
|<span data-ttu-id="d125e-291">PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="d125e-291">PR_ADDRTYPE_W</span></span>  <br/> |<span data-ttu-id="d125e-292">0x3002001F</span><span class="sxs-lookup"><span data-stu-id="d125e-292">0x3002001F</span></span>  <br/> |<span data-ttu-id="d125e-293">Type d’adresse du destinataire (par exemple, SMTP ou EX).</span><span class="sxs-lookup"><span data-stu-id="d125e-293">The recipient's address type (e.g. SMTP or EX).</span></span>  <br/> |
|<span data-ttu-id="d125e-294">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="d125e-294">PR_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="d125e-295">0x300B0102</span><span class="sxs-lookup"><span data-stu-id="d125e-295">0x300B0102</span></span>  <br/> |<span data-ttu-id="d125e-296">Clé de recherche MAPI du destinataire.</span><span class="sxs-lookup"><span data-stu-id="d125e-296">The recipient's MAPI search key.</span></span>  <br/> |
|<span data-ttu-id="d125e-297">PR_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="d125e-297">PR_SMTP_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="d125e-298">0x39FE001f</span><span class="sxs-lookup"><span data-stu-id="d125e-298">0x39FE001f</span></span>  <br/> |<span data-ttu-id="d125e-299">Adresse SMTP du destinataire.</span><span class="sxs-lookup"><span data-stu-id="d125e-299">The recipient's SMTP address.</span></span>  <br/> |
|<span data-ttu-id="d125e-300">PR_DROPDOWN_DISPLAY_NAME_W (non transmis aux destinataires, spécifiques uniquement aux flux de saisie semi-automatique)</span><span class="sxs-lookup"><span data-stu-id="d125e-300">PR_DROPDOWN_DISPLAY_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="d125e-301">0X6003001f</span><span class="sxs-lookup"><span data-stu-id="d125e-301">0X6003001f</span></span>  <br/> |<span data-ttu-id="d125e-302">La chaîne d’affichage qui s’affiche dans la liste de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="d125e-302">The display string that appears in the autocomplete list.</span></span>  <br/> |
|<span data-ttu-id="d125e-303">PR_NICK_NAME_WEIGHT (non transmis aux destinataires, spécifiques uniquement aux flux de saisie semi-automatique)</span><span class="sxs-lookup"><span data-stu-id="d125e-303">PR_NICK_NAME_WEIGHT (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="d125e-304">0x60040003</span><span class="sxs-lookup"><span data-stu-id="d125e-304">0x60040003</span></span>  <br/> |<span data-ttu-id="d125e-305">La pondération de cette entrée de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="d125e-305">The weight of this autocomplete entry.</span></span> <span data-ttu-id="d125e-306">La pondération est utilisée pour déterminer dans quel ordre les entrées de saisie semi-automatique se produisent lorsqu’elles correspondent à la liste de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="d125e-306">The weight is used to determine in what order autocomplete entries occur when matching the autocomplete list.</span></span> <span data-ttu-id="d125e-307">Les entrées ayant une pondération supérieure s’affichent avant les entrées ayant une pondération inférieure.</span><span class="sxs-lookup"><span data-stu-id="d125e-307">Entries with higher weight will show before entries with lower weight.</span></span> <span data-ttu-id="d125e-308">La liste complète de saisie semi-automatique est triée par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d125e-308">The complete autocomplete list is sorted by this property.</span></span> <span data-ttu-id="d125e-309">La pondération diminue régulièrement au fil du temps et augmente lorsque l’utilisateur envoie un message électronique à ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="d125e-309">The weight periodically decreases over time and increases when the user sends an email to this recipient.</span></span> <span data-ttu-id="d125e-310">Consultez la description plus loin dans cette rubrique pour plus d’informations sur cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d125e-310">See the description later in this topic for more information about this property.</span></span>  <br/> |
   
<span data-ttu-id="d125e-311">PR_NICK_NAME_WEIGHT</span><span class="sxs-lookup"><span data-stu-id="d125e-311">PR_NICK_NAME_WEIGHT</span></span>
  
<span data-ttu-id="d125e-312">L’ensemble de lignes dans le flux de saisie semi-automatique est trié dans l’ordre décroissant par la propriété PR_NICK_NAME_WEIGHT et le flux de saisie semi-automatique doit toujours conserver cette caractéristique triée.</span><span class="sxs-lookup"><span data-stu-id="d125e-312">The set of rows in the autocomplete stream is sorted in descending order by the PR_NICK_NAME_WEIGHT property and the autocomplete stream should always preserve this sorted characteristic.</span></span> <span data-ttu-id="d125e-313">Par conséquent, les modifications apportées à la pondération de ligne doivent également assurer que la position de la ligne conserve l’ordre trié de l’ensemble complet de lignes.</span><span class="sxs-lookup"><span data-stu-id="d125e-313">Therefore, any changes to a row's weight should also ensure that the row's position maintains the sorted order of the complete set of rows.</span></span> <span data-ttu-id="d125e-314">Les ajouts apportés à l’ensemble de ligne doivent être insérés à l’emplacement correct afin de conserver l’ordre trié.</span><span class="sxs-lookup"><span data-stu-id="d125e-314">Any additions to the row-set should be inserted to the correct position to maintain the sorted order.</span></span>
  
<span data-ttu-id="d125e-315">La valeur minimale de cette pondération est 0 x 1 et la valeur maximale est LONG_MAX.</span><span class="sxs-lookup"><span data-stu-id="d125e-315">The minimum value of this weight is 0x1 and the maximum value is LONG_MAX.</span></span> <span data-ttu-id="d125e-316">Toutes les autres valeurs concernant la pondération sont considérées comme non valides.</span><span class="sxs-lookup"><span data-stu-id="d125e-316">Any other values for the weight are considered invalid.</span></span>
  
<span data-ttu-id="d125e-317">Lorsqu’Outlook 2007 envoie un courrier ou résout un destinataire, il augmentera la pondération du destinataire par 0 x 2000.</span><span class="sxs-lookup"><span data-stu-id="d125e-317">When Outlook 2007 sends a mail to or resolves a recipient, it will increase that recipient's weight by 0x2000.</span></span>
  

