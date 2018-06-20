---
title: Flux de saisie semi-automatique
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7fc1fae4ed648d59c273b20ced247f6d20e01a6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782977"
---
# <a name="autocomplete-stream"></a><span data-ttu-id="e0b6c-103">Flux de saisie semi-automatique</span><span class="sxs-lookup"><span data-stu-id="e0b6c-103">Autocomplete Stream</span></span>

  
  
<span data-ttu-id="e0b6c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e0b6c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e0b6c-105">En plus de savoir comment Microsoft Outlook interagit avec le flux de saisie semi-automatique, vous devez également comprendre le format binaire de l’objet stream de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-105">In addition to knowing how Microsoft Outlook interacts with the autocomplete stream, you must also understand the binary format of the autocomplete stream.</span></span>
  
<span data-ttu-id="e0b6c-106">Le flux de saisie semi-automatique est un ensemble de lignes de propriété de destinataire qui sont enregistrés sous la forme d’un flux binaire avec des métadonnées de référence qui sont utilisé uniquement par Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007 et Microsoft Outlook 2003.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-106">The autocomplete stream is a set of recipient property rows that are saved as a binary stream together with some bookkeeping metadata that is used only by Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007, and Microsoft Outlook 2003.</span></span> <span data-ttu-id="e0b6c-107">Les métadonnées sont pertinentes pour les interactions d’Outlook avec le flux de saisie semi-automatique afin que les tierces parties doit conserver Nouveautés dans chaque bloc de métadonnées lorsqu’ils enregistrent un flux de saisie semi-automatique modifié.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-107">The metadata is relevant to Outlook interactions with the autocomplete stream so third parties must preserve what is in each metadata block when they save a modified autocomplete stream.</span></span> <span data-ttu-id="e0b6c-108">En d’autres termes, les tierces parties doit modifier uniquement la partie de l’ensemble de lignes du format binaire et de conserver ce qui a déjà été dans les blocs de métadonnées de l’objet stream de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-108">In other words, third parties should modify only the row-set part of the binary format and preserve what was already in the metadata blocks of the autocomplete stream.</span></span>
  
## <a name="stream-visualization"></a><span data-ttu-id="e0b6c-109">Visualisation du flux de données</span><span class="sxs-lookup"><span data-stu-id="e0b6c-109">Stream Visualization</span></span>

<span data-ttu-id="e0b6c-110">La disposition de haut niveau de l’objet stream de saisie semi-automatique est la suivante :</span><span class="sxs-lookup"><span data-stu-id="e0b6c-110">The high-level layout of the autocomplete stream is as follows:</span></span>
  
<span data-ttu-id="e0b6c-111">Métadonnées (4 octets)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-111">Metadata (4 bytes)</span></span>
  
<span data-ttu-id="e0b6c-112">Numéro de Version principale (4 octets)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-112">Major Version Number (4 bytes)</span></span>
  
<span data-ttu-id="e0b6c-113">Numéro de Version secondaire (4 octets)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-113">Minor Version Number (4 bytes)</span></span>
  
<span data-ttu-id="e0b6c-114">Nombre de lignes n (4 octets)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-114">Number of rows n (4 bytes)</span></span>
  
<span data-ttu-id="e0b6c-115">Nombre de propriétés p dans la ligne 1 (4 octets)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-115">Number of properties p in row one (4 bytes)</span></span>
  
<span data-ttu-id="e0b6c-116">Balise de propriété propriété 1 (4 octets)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-116">Property 1's property tag (4 bytes)</span></span>
  
<span data-ttu-id="e0b6c-117">Propriété 1 du réservée données (4 octets)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-117">Property 1's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="e0b6c-118">Union de valeur de propriété 1 (8 octets)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-118">Property 1's value union (8 bytes)</span></span>
  
<span data-ttu-id="e0b6c-119">Données de valeur de propriété 1 (0 ou variables octets)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-119">Property 1's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="e0b6c-120">…</span><span class="sxs-lookup"><span data-stu-id="e0b6c-120"></span></span> <span data-ttu-id="e0b6c-121">(propriété 2 par le biais de la propriété P-1)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-121">(property 2 through property P-1)</span></span>
  
<span data-ttu-id="e0b6c-122">Balise de propriété de la propriété du p (4 octets)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-122">Property p's property tag (4 bytes)</span></span>
  
<span data-ttu-id="e0b6c-123">Propriété p de réservé à des données (4 octets)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-123">Property p's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="e0b6c-124">Union de valeur de propriété de p (8 octets)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-124">Property p's value union (8 bytes)</span></span>
  
<span data-ttu-id="e0b6c-125">Données de la propriété de p la valeur (0 ou variables octets)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-125">Property p's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="e0b6c-126">Nombre de propriétés q de la deuxième ligne (4 octets)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-126">Number of properties q in row two (4 bytes)</span></span>
  
<span data-ttu-id="e0b6c-127">…</span><span class="sxs-lookup"><span data-stu-id="e0b6c-127"></span></span> <span data-ttu-id="e0b6c-128">(deux propriétés de ligne)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-128">(row two's properties)</span></span>
  
<span data-ttu-id="e0b6c-129">…</span><span class="sxs-lookup"><span data-stu-id="e0b6c-129"></span></span> <span data-ttu-id="e0b6c-130">(ligne 3 à n-1 de la ligne)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-130">(row 3 through row n-1)</span></span>
  
<span data-ttu-id="e0b6c-131">Nombre de propriétés r ligne n (4 octets)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-131">Number of properties r in row n (4 bytes)</span></span>
  
<span data-ttu-id="e0b6c-132">…</span><span class="sxs-lookup"><span data-stu-id="e0b6c-132"></span></span> <span data-ttu-id="e0b6c-133">(ligne n's propriétés)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-133">(row n's properties)</span></span>
  
<span data-ttu-id="e0b6c-134">Nombre d’octets des informations supplémentaires eu (4 octets)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-134">Extra information byte count EI (4 bytes)</span></span>
  
<span data-ttu-id="e0b6c-135">Informations supplémentaires (octets eu)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-135">Extra information (EI bytes)</span></span>
  
<span data-ttu-id="e0b6c-136">Métadonnées (8 octets)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-136">Metadata (8 bytes)</span></span>
  
<span data-ttu-id="e0b6c-137">Pour obtenir un exemple d’une structure binaire, voir exemple binaires dans les [Format de fichier NK2 Outlook 2003/2007 et des instructions pour les développeurs.](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-137">For an example of a binary structure, see Binary Example in the [Outlook 2003/2007 NK2 File Format and Developer Guidelines.](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span></span>
  
## <a name="high-level-layout"></a><span data-ttu-id="e0b6c-138">Disposition de haut niveau</span><span class="sxs-lookup"><span data-stu-id="e0b6c-138">High-level Layout</span></span>

<span data-ttu-id="e0b6c-139">D’une manière générale, la mise en page de l’objet stream de saisie semi-automatique est la suivante :</span><span class="sxs-lookup"><span data-stu-id="e0b6c-139">Broadly speaking, the layout of the autocomplete stream is as follows:</span></span>
  
|<span data-ttu-id="e0b6c-140">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-140">**Value Data**</span></span>|<span data-ttu-id="e0b6c-141">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-141">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0b6c-142">Métadonnées</span><span class="sxs-lookup"><span data-stu-id="e0b6c-142">Metadata</span></span>  <br/> |<span data-ttu-id="e0b6c-143">4</span><span class="sxs-lookup"><span data-stu-id="e0b6c-143">4</span></span>  <br/> |
|<span data-ttu-id="e0b6c-144">Numéro de Version majeure</span><span class="sxs-lookup"><span data-stu-id="e0b6c-144">Major Version Number</span></span>  <br/> |<span data-ttu-id="e0b6c-145">4</span><span class="sxs-lookup"><span data-stu-id="e0b6c-145">4</span></span>  <br/> |
|<span data-ttu-id="e0b6c-146">Numéro de Version secondaire</span><span class="sxs-lookup"><span data-stu-id="e0b6c-146">Minor Version Number</span></span>  <br/> |<span data-ttu-id="e0b6c-147">4</span><span class="sxs-lookup"><span data-stu-id="e0b6c-147">4</span></span>  <br/> |
|<span data-ttu-id="e0b6c-148">Ensemble de lignes</span><span class="sxs-lookup"><span data-stu-id="e0b6c-148">Row-set</span></span>  <br/> |<span data-ttu-id="e0b6c-149">Variable</span><span class="sxs-lookup"><span data-stu-id="e0b6c-149">Variable</span></span>  <br/> |
|<span data-ttu-id="e0b6c-150">Nombre d’octets des informations supplémentaires eu</span><span class="sxs-lookup"><span data-stu-id="e0b6c-150">Extra information byte count EI</span></span>  <br/> |<span data-ttu-id="e0b6c-151">4</span><span class="sxs-lookup"><span data-stu-id="e0b6c-151">4</span></span>  <br/> |
|<span data-ttu-id="e0b6c-152">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e0b6c-152">Extra information</span></span>  <br/> |<span data-ttu-id="e0b6c-153">EU</span><span class="sxs-lookup"><span data-stu-id="e0b6c-153">EI</span></span>  <br/> |
|<span data-ttu-id="e0b6c-154">Métadonnées</span><span class="sxs-lookup"><span data-stu-id="e0b6c-154">Metadata</span></span>  <br/> |<span data-ttu-id="e0b6c-155">8</span><span class="sxs-lookup"><span data-stu-id="e0b6c-155">8</span></span>  <br/> |
   
<span data-ttu-id="e0b6c-156">Lors de la lecture de ce flux, si la version principale est différente de 12, puis ce flux ne doit pas être lu ou écrit.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-156">When reading this stream, if the major version is different than 12, then this stream should not be read or written.</span></span> <span data-ttu-id="e0b6c-157">La version secondaire actuelle du flux de saisie semi-automatique est 0, ce qui a la valeur 0 le nombre d’octets d’informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-157">The current minor version of the autocomplete stream is 0, which has the Extra Information Byte count set to 0.</span></span> <span data-ttu-id="e0b6c-158">Si la version secondaire est différente de 0, puis il y aura plus d’informations dans les informations supplémentaires qui doivent être lu lors de la lecture du flux et conservées lors de l’écriture du flux.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-158">If the minor version is different than 0, then there will be information in the extra information that needs to be read when reading the stream and preserved when writing the stream.</span></span> <span data-ttu-id="e0b6c-159">La version secondaire vous devrez également être conservées lors de l’écriture de l’objet stream.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-159">The minor version will also need to be preserved when writing the stream.</span></span> <span data-ttu-id="e0b6c-160">Si ces deux éléments ne sont pas conservées, les instances d’Outlook qui écrit les informations supplémentaires perdre des données.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-160">If both of these are not preserved, instances of Outlook that wrote the extra information will lose data.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e0b6c-161">Les applications ne doivent pas ajouter des données personnalisées dans le champ informations supplémentaires ou de modifier la version secondaire que cette fonctionnalité est pour prendre en charge des extensions Outlook vers le format et tiers arbitraires.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-161">Applications must not add custom data to the Extra Information field or change the minor version as this functionality is to support Outlook extensions to the format and not arbitrary third-party extensions.</span></span> 
  
## <a name="row-set-layout"></a><span data-ttu-id="e0b6c-162">Disposition de l’ensemble de lignes</span><span class="sxs-lookup"><span data-stu-id="e0b6c-162">Row-set Layout</span></span>

<span data-ttu-id="e0b6c-163">La disposition de l’ensemble de lignes est la suivante :</span><span class="sxs-lookup"><span data-stu-id="e0b6c-163">The row-set layout is as follows:</span></span> 
  
|<span data-ttu-id="e0b6c-164">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-164">**Value Data**</span></span>|<span data-ttu-id="e0b6c-165">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-165">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0b6c-166">Nombre de lignes</span><span class="sxs-lookup"><span data-stu-id="e0b6c-166">Number of rows</span></span>  <br/> |<span data-ttu-id="e0b6c-167">4</span><span class="sxs-lookup"><span data-stu-id="e0b6c-167">4</span></span>  <br/> |
|<span data-ttu-id="e0b6c-168">Objet Rows</span><span class="sxs-lookup"><span data-stu-id="e0b6c-168">Rows</span></span>  <br/> |<span data-ttu-id="e0b6c-169">Variable</span><span class="sxs-lookup"><span data-stu-id="e0b6c-169">Variable</span></span>  <br/> |
   
<span data-ttu-id="e0b6c-170">Le nombre de lignes identifie le nombre de lignes fournis dans la partie suivante de la séquence de flux binaire.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-170">The number of rows identifies how many rows come in the next part of the binary stream sequence.</span></span>
  
## <a name="row-layout"></a><span data-ttu-id="e0b6c-171">Mise en ligne</span><span class="sxs-lookup"><span data-stu-id="e0b6c-171">Row Layout</span></span>

<span data-ttu-id="e0b6c-172">Chaque ligne est au format suivant :</span><span class="sxs-lookup"><span data-stu-id="e0b6c-172">Each row is of the following format:</span></span>
  
|<span data-ttu-id="e0b6c-173">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-173">**Value Data**</span></span>|<span data-ttu-id="e0b6c-174">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-174">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0b6c-175">Nombre de propriétés</span><span class="sxs-lookup"><span data-stu-id="e0b6c-175">Number of properties</span></span>  <br/> |<span data-ttu-id="e0b6c-176">4</span><span class="sxs-lookup"><span data-stu-id="e0b6c-176">4</span></span>  <br/> |
|<span data-ttu-id="e0b6c-177">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e0b6c-177">Properties</span></span>  <br/> |<span data-ttu-id="e0b6c-178">Variable</span><span class="sxs-lookup"><span data-stu-id="e0b6c-178">Variable</span></span>  <br/> |
   
<span data-ttu-id="e0b6c-179">Le nombre de propriétés identifie le nombre de propriétés fournis dans la partie suivante de la séquence de flux binaire.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-179">The number of properties identifies how many properties come in the next part of the binary stream sequence.</span></span>
  
## <a name="property-layout"></a><span data-ttu-id="e0b6c-180">Propriété Layout</span><span class="sxs-lookup"><span data-stu-id="e0b6c-180">Property Layout</span></span>

<span data-ttu-id="e0b6c-181">Chaque propriété est au format suivant :</span><span class="sxs-lookup"><span data-stu-id="e0b6c-181">Each property is of the following format:</span></span>
  
|<span data-ttu-id="e0b6c-182">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-182">**Value Data**</span></span>|<span data-ttu-id="e0b6c-183">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-183">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0b6c-184">Balise de propriété</span><span class="sxs-lookup"><span data-stu-id="e0b6c-184">Property Tag</span></span>  <br/> |<span data-ttu-id="e0b6c-185">4</span><span class="sxs-lookup"><span data-stu-id="e0b6c-185">4</span></span>  <br/> |
|<span data-ttu-id="e0b6c-186">Données réservé</span><span class="sxs-lookup"><span data-stu-id="e0b6c-186">Reserved Data</span></span>  <br/> |<span data-ttu-id="e0b6c-187">4</span><span class="sxs-lookup"><span data-stu-id="e0b6c-187">4</span></span>  <br/> |
|<span data-ttu-id="e0b6c-188">Propriété valeur Union</span><span class="sxs-lookup"><span data-stu-id="e0b6c-188">Property Value Union</span></span>  <br/> ||
|<span data-ttu-id="e0b6c-189">Données de la valeur</span><span class="sxs-lookup"><span data-stu-id="e0b6c-189">Value Data</span></span>  <br/> |<span data-ttu-id="e0b6c-190">0 ou variable (en fonction de la balise de propriétés)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-190">0 or variable (depending on the prop tag)</span></span>  <br/> |
   
## <a name="interpreting-the-property-value"></a><span data-ttu-id="e0b6c-191">Interprétation de la valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="e0b6c-191">Interpreting the Property Value</span></span>

<span data-ttu-id="e0b6c-192">L’Union de valeur de propriété et la valeur des données sont à être interprété en fonction de la balise de propriété dans les premières 4 octets du bloc de propriété.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-192">The Property Value Union and the Value Data are to be interpreted based on the property tag in the first 4 bytes of the property block.</span></span> <span data-ttu-id="e0b6c-193">Cette balise de propriété est dans le même format qu’une balise de propriété MAPI.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-193">This property tag is in the same format as a MAPI property tag.</span></span> <span data-ttu-id="e0b6c-194">Bits 0 à 15 de la balise de propriété sont le type de propriété.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-194">Bits 0 through 15 of the property tag are the property's type.</span></span> <span data-ttu-id="e0b6c-195">Bits 16 à 31 sont l’identificateur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-195">Bits 16 through 31 are the property's identifier.</span></span> <span data-ttu-id="e0b6c-196">Le type de propriété détermine la façon dont le reste de la propriété doit être lu.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-196">The property type determines how the rest of the property should be read.</span></span>
  
## <a name="static-value"></a><span data-ttu-id="e0b6c-197">Valeur statique</span><span class="sxs-lookup"><span data-stu-id="e0b6c-197">Static Value</span></span>

<span data-ttu-id="e0b6c-198">Certaines propriétés n’ont aucune donnée de valeur et contiennent uniquement des données dans l’union.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-198">Some properties have no Value Data and only have data in the union.</span></span> <span data-ttu-id="e0b6c-199">Les types de propriété suivants (qui proviennent de la balise de propriété) doivent interpréter les données de propriété Union 8 octets comme suit :</span><span class="sxs-lookup"><span data-stu-id="e0b6c-199">The following property types (which come from the Property Tag) should interpret the 8-byte Property Union data as follows:</span></span>
  
|<span data-ttu-id="e0b6c-200">**Type de propriétés**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-200">**Prop Type**</span></span>|<span data-ttu-id="e0b6c-201">**Propriété interprétation Union**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-201">**Property Union Interpretation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0b6c-202">PT_I2</span><span class="sxs-lookup"><span data-stu-id="e0b6c-202">PT_I2</span></span>  <br/> |<span data-ttu-id="e0b6c-203">int court</span><span class="sxs-lookup"><span data-stu-id="e0b6c-203">short int</span></span>  <br/> |
|<span data-ttu-id="e0b6c-204">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e0b6c-204">PT_LONG</span></span>  <br/> |<span data-ttu-id="e0b6c-205">long</span><span class="sxs-lookup"><span data-stu-id="e0b6c-205">long</span></span>  <br/> |
|<span data-ttu-id="e0b6c-206">PT_R4</span><span class="sxs-lookup"><span data-stu-id="e0b6c-206">PT_R4</span></span>  <br/> |<span data-ttu-id="e0b6c-207">flottant</span><span class="sxs-lookup"><span data-stu-id="e0b6c-207">float</span></span>  <br/> |
|<span data-ttu-id="e0b6c-208">PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="e0b6c-208">PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="e0b6c-209">double</span><span class="sxs-lookup"><span data-stu-id="e0b6c-209">double</span></span>  <br/> |
|<span data-ttu-id="e0b6c-210">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e0b6c-210">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="e0b6c-211">int court</span><span class="sxs-lookup"><span data-stu-id="e0b6c-211">short int</span></span>  <br/> |
|<span data-ttu-id="e0b6c-212">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e0b6c-212">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="e0b6c-213">FILETIME</span><span class="sxs-lookup"><span data-stu-id="e0b6c-213">FILETIME</span></span>  <br/> |
|<span data-ttu-id="e0b6c-214">PT_I8</span><span class="sxs-lookup"><span data-stu-id="e0b6c-214">PT_I8</span></span>  <br/> |<span data-ttu-id="e0b6c-215">LARGE_INTEGER</span><span class="sxs-lookup"><span data-stu-id="e0b6c-215">LARGE_INTEGER</span></span>  <br/> |
   
## <a name="dynamic-values"></a><span data-ttu-id="e0b6c-216">Valeurs dynamiques</span><span class="sxs-lookup"><span data-stu-id="e0b6c-216">Dynamic Values</span></span>

<span data-ttu-id="e0b6c-217">Autres propriétés disposent données dans un bloc de données de la valeur après que les premières 16 octets qui contiennent la balise de propriété, les données réservés et l’Union de valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-217">Other properties have data in a Value Data block after the first 16 bytes that contain the Property Tag, the Reserved Data, and the Property Value Union.</span></span> <span data-ttu-id="e0b6c-218">Contrairement aux valeurs statiques, les données stockées dans l’union de la valeur de la propriété 8 octets sont sans effet sur la lecture.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-218">Unlike static values, the data that is stored in the 8-byte Property Value union is irrelevant on reading.</span></span> <span data-ttu-id="e0b6c-219">Lors de l’écriture, assurez-vous que vous remplissez ces 8 octets avec un élément.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-219">When writing, make sure that you fill these 8 bytes with something.</span></span> <span data-ttu-id="e0b6c-220">Toutefois, le contenu de 8 octets n’est pas important.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-220">However, the content of the 8 bytes is not important.</span></span> <span data-ttu-id="e0b6c-221">Dans les valeurs dynamiques, type de la balise de propriété détermine comment interpréter les données de la valeur.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-221">In dynamic values, the property tag's type determines how to interpret the Value Data.</span></span>
  
<span data-ttu-id="e0b6c-222">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="e0b6c-222">PT_STRING8</span></span> 
  
|<span data-ttu-id="e0b6c-223">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-223">**Value Data**</span></span>|<span data-ttu-id="e0b6c-224">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-224">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0b6c-225">Nombre d’octets n</span><span class="sxs-lookup"><span data-stu-id="e0b6c-225">Number of bytes n</span></span>  <br/> |<span data-ttu-id="e0b6c-226">4</span><span class="sxs-lookup"><span data-stu-id="e0b6c-226">4</span></span>  <br/> |
|<span data-ttu-id="e0b6c-227">Octets à être interprété comme une chaîne ANSI (y compris le terminateur NULL)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-227">Bytes to be interpreted as an ANSI string (includes NULL terminator)</span></span>  <br/> |<span data-ttu-id="e0b6c-228">n</span><span class="sxs-lookup"><span data-stu-id="e0b6c-228">n</span></span>  <br/> |
   
<span data-ttu-id="e0b6c-229">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="e0b6c-229">PT_CLSID</span></span>
  
|<span data-ttu-id="e0b6c-230">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-230">**Value Data**</span></span>|<span data-ttu-id="e0b6c-231">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-231">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0b6c-232">Octets à être interprété comme un GUID</span><span class="sxs-lookup"><span data-stu-id="e0b6c-232">Bytes to be interpreted as a GUID</span></span>  <br/> |<span data-ttu-id="e0b6c-233">16</span><span class="sxs-lookup"><span data-stu-id="e0b6c-233">16</span></span>  <br/> |
|||
   
<span data-ttu-id="e0b6c-234">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e0b6c-234">PT_BINARY</span></span> 
  
|<span data-ttu-id="e0b6c-235">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-235">**Value Data**</span></span>|<span data-ttu-id="e0b6c-236">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-236">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0b6c-237">Nombre d’octets n</span><span class="sxs-lookup"><span data-stu-id="e0b6c-237">Number of bytes n</span></span>  <br/> |<span data-ttu-id="e0b6c-238">4</span><span class="sxs-lookup"><span data-stu-id="e0b6c-238">4</span></span>  <br/> |
|<span data-ttu-id="e0b6c-239">Octets à être interprété comme un tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="e0b6c-239">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="e0b6c-240">n</span><span class="sxs-lookup"><span data-stu-id="e0b6c-240">n</span></span>  <br/> |
   
<span data-ttu-id="e0b6c-241">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="e0b6c-241">PT_ERROR</span></span>
  
|<span data-ttu-id="e0b6c-242">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-242">**Value Data**</span></span>|<span data-ttu-id="e0b6c-243">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-243">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0b6c-244">Nombre d’octets n</span><span class="sxs-lookup"><span data-stu-id="e0b6c-244">Number of bytes n</span></span>  <br/> |<span data-ttu-id="e0b6c-245">4</span><span class="sxs-lookup"><span data-stu-id="e0b6c-245">4</span></span>  <br/> |
|<span data-ttu-id="e0b6c-246">Octets à être interprété comme un tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="e0b6c-246">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="e0b6c-247">n</span><span class="sxs-lookup"><span data-stu-id="e0b6c-247">n</span></span>  <br/> |
   
<span data-ttu-id="e0b6c-248">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="e0b6c-248">PT_MV_BINARY</span></span>
  
|<span data-ttu-id="e0b6c-249">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-249">**Value Data**</span></span>|<span data-ttu-id="e0b6c-250">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-250">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0b6c-251">Nombre de tableaux binaires X</span><span class="sxs-lookup"><span data-stu-id="e0b6c-251">Number of binary arrays X</span></span>  <br/> |<span data-ttu-id="e0b6c-252">4</span><span class="sxs-lookup"><span data-stu-id="e0b6c-252">4</span></span>  <br/> |
|<span data-ttu-id="e0b6c-253">A exécuter d’octets contenant X tableaux binaires.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-253">A run of bytes that contains X binary arrays.</span></span> <span data-ttu-id="e0b6c-254">Chaque tableau doit être interprété comme l’octet PT_BINARY exécuter.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-254">Each array should be interpreted exactly like the PT_BINARY byte run.</span></span>  <br/> |<span data-ttu-id="e0b6c-255">Variable</span><span class="sxs-lookup"><span data-stu-id="e0b6c-255">Variable</span></span>  <br/> |
   
<span data-ttu-id="e0b6c-256">PT_MV_STRING8 (Outlook 2007, Outlook 2010 et Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-256">PT_MV_STRING8 (Outlook 2007, Outlook 2010, and Outlook 2013)</span></span>
  
|<span data-ttu-id="e0b6c-257">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-257">**Value Data**</span></span>|<span data-ttu-id="e0b6c-258">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-258">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0b6c-259">Nombre de chaînes ANSI X</span><span class="sxs-lookup"><span data-stu-id="e0b6c-259">Number of ANSI strings X</span></span>  <br/> |<span data-ttu-id="e0b6c-260">4</span><span class="sxs-lookup"><span data-stu-id="e0b6c-260">4</span></span>  <br/> |
|<span data-ttu-id="e0b6c-261">Une séquence d’octets qui contient les chaînes ANSI X.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-261">A run of bytes that contains X ANSI strings.</span></span> <span data-ttu-id="e0b6c-262">Chaque chaîne doit être interprété comme l’octet PT_STRING8 exécuter.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-262">Each string should be interpreted exactly like the PT_STRING8 byte run.</span></span>  <br/> |<span data-ttu-id="e0b6c-263">Variable</span><span class="sxs-lookup"><span data-stu-id="e0b6c-263">Variable</span></span>  <br/> |
   
<span data-ttu-id="e0b6c-264">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-264">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span></span>
  
|<span data-ttu-id="e0b6c-265">**Données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-265">**Value Data**</span></span>|<span data-ttu-id="e0b6c-266">**Nombre d’octets**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-266">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0b6c-267">Nombre de chaînes UNICODE X</span><span class="sxs-lookup"><span data-stu-id="e0b6c-267">Number of UNICODE strings X</span></span>  <br/> |<span data-ttu-id="e0b6c-268">4</span><span class="sxs-lookup"><span data-stu-id="e0b6c-268">4</span></span>  <br/> |
|<span data-ttu-id="e0b6c-269">Une séquence d’octets qui contient les chaînes X UNICODE.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-269">A run of bytes that contains X UNICODE strings.</span></span> <span data-ttu-id="e0b6c-270">Chaque chaîne doit être interprété comme l’octet PT_UNICODE exécuter.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-270">Each string should be interpreted exactly like the PT_UNICODE byte run.</span></span>  <br/> |<span data-ttu-id="e0b6c-271">Variable</span><span class="sxs-lookup"><span data-stu-id="e0b6c-271">Variable</span></span>  <br/> |
   
## <a name="significant-properties"></a><span data-ttu-id="e0b6c-272">Propriétés importantes</span><span class="sxs-lookup"><span data-stu-id="e0b6c-272">Significant properties</span></span>

<span data-ttu-id="e0b6c-273">Comme mentionné précédemment dans cette rubrique, les blocs binaires qui représentent les propriétés ont des balises de propriété qui correspondent aux propriétés de destinataires de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-273">As mentioned previously in this topic, the binary blocks that represent properties have property tags that correspond to properties on address book recipients.</span></span> <span data-ttu-id="e0b6c-274">Pour les propriétés qui ne sont pas répertoriées ici, vous pouvez consulter la description de la propriété à http://msdn.microsoft.com/en-us/library/cc433490(EXCHG.80).aspx.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-274">For properties that are not listed here, you can look up the property description at http://msdn.microsoft.com/en-us/library/cc433490(EXCHG.80).aspx.</span></span>
  
|<span data-ttu-id="e0b6c-275">**Nom de la propriété**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-275">**Property Name**</span></span>|<span data-ttu-id="e0b6c-276">**Balise de propriété**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-276">**Property Tag**</span></span>|<span data-ttu-id="e0b6c-277">**Description (pour plus d’informations, voir MSDN)**</span><span class="sxs-lookup"><span data-stu-id="e0b6c-277">**Description (see MSDN for more information)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e0b6c-278">PR_NICK_NAME_W (ne pas transmis sur les destinataires, spécifiques aux flux de saisie semi-automatique uniquement)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-278">PR_NICK_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="e0b6c-279">0x6001001f</span><span class="sxs-lookup"><span data-stu-id="e0b6c-279">0x6001001f</span></span>  <br/> |<span data-ttu-id="e0b6c-280">Cette propriété doit être la première dans chaque ligne du destinataire.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-280">This property must be first in each recipient row.</span></span> <span data-ttu-id="e0b6c-281">Elle sert fonctionnellement un identificateur de clé pour la ligne du destinataire.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-281">It functionally serves as a key identifier for the recipient row.</span></span>  <br/> |
|<span data-ttu-id="e0b6c-282">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e0b6c-282">PR_ENTRYID</span></span>  <br/> |<span data-ttu-id="e0b6c-283">0x0FFF0102</span><span class="sxs-lookup"><span data-stu-id="e0b6c-283">0x0FFF0102</span></span>  <br/> |<span data-ttu-id="e0b6c-284">L’identificateur d’entrée adresse téléchargeable pour le destinataire.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-284">The address book entry identifier for the recipient.</span></span>  <br/> |
|<span data-ttu-id="e0b6c-285">PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="e0b6c-285">PR_DISPLAY_NAME_W</span></span>  <br/> |<span data-ttu-id="e0b6c-286">0x3001001F</span><span class="sxs-lookup"><span data-stu-id="e0b6c-286">0x3001001F</span></span>  <br/> |<span data-ttu-id="e0b6c-287">Nom d’affichage du destinataire.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-287">The recipient's display name.</span></span>  <br/> |
|<span data-ttu-id="e0b6c-288">PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="e0b6c-288">PR_EMAIL_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="e0b6c-289">0x3003001F</span><span class="sxs-lookup"><span data-stu-id="e0b6c-289">0x3003001F</span></span>  <br/> |<span data-ttu-id="e0b6c-290">Adresse de messagerie du destinataire (par exemple johndoe@contoso.com ou/o = Contoso/OU = Foo/cn = Recipients/cn = johndoe)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-290">The recipient's email address (e.g. johndoe@contoso.com or /o=Contoso/OU=Foo/cn=Recipients/cn=johndoe)</span></span>  <br/> |
|<span data-ttu-id="e0b6c-291">PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="e0b6c-291">PR_ADDRTYPE_W</span></span>  <br/> |<span data-ttu-id="e0b6c-292">0x3002001F</span><span class="sxs-lookup"><span data-stu-id="e0b6c-292">0x3002001F</span></span>  <br/> |<span data-ttu-id="e0b6c-293">Type d’adresse du destinataire (par exemple, SMTP ou EX).</span><span class="sxs-lookup"><span data-stu-id="e0b6c-293">The recipient's address type (e.g. SMTP or EX).</span></span>  <br/> |
|<span data-ttu-id="e0b6c-294">CLÉ PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="e0b6c-294">PR_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="e0b6c-295">0x300B0102</span><span class="sxs-lookup"><span data-stu-id="e0b6c-295">0x300B0102</span></span>  <br/> |<span data-ttu-id="e0b6c-296">Clé de recherche MAPI du destinataire.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-296">The recipient's MAPI search key.</span></span>  <br/> |
|<span data-ttu-id="e0b6c-297">PR_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="e0b6c-297">PR_SMTP_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="e0b6c-298">0x39FE001f</span><span class="sxs-lookup"><span data-stu-id="e0b6c-298">0x39FE001f</span></span>  <br/> |<span data-ttu-id="e0b6c-299">L’adresse du destinataire SMTP.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-299">The recipient's SMTP address.</span></span>  <br/> |
|<span data-ttu-id="e0b6c-300">PR_DROPDOWN_DISPLAY_NAME_W (ne pas transmis sur les destinataires, spécifiques aux flux de saisie semi-automatique uniquement)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-300">PR_DROPDOWN_DISPLAY_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="e0b6c-301">0X6003001f</span><span class="sxs-lookup"><span data-stu-id="e0b6c-301">0X6003001f</span></span>  <br/> |<span data-ttu-id="e0b6c-302">La chaîne d’affichage qui apparaît dans la liste de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-302">The display string that appears in the autocomplete list.</span></span>  <br/> |
|<span data-ttu-id="e0b6c-303">PR_NICK_NAME_WEIGHT (ne pas transmis sur les destinataires, spécifiques aux flux de saisie semi-automatique uniquement)</span><span class="sxs-lookup"><span data-stu-id="e0b6c-303">PR_NICK_NAME_WEIGHT (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="e0b6c-304">0x60040003</span><span class="sxs-lookup"><span data-stu-id="e0b6c-304">0x60040003</span></span>  <br/> |<span data-ttu-id="e0b6c-305">Le poids de cette entrée de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-305">The weight of this autocomplete entry.</span></span> <span data-ttu-id="e0b6c-306">Le poids est utilisé pour déterminer dans quel saisie semi-automatique ordre entrées se produisent lors de la recherche de la liste de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-306">The weight is used to determine in what order autocomplete entries occur when matching the autocomplete list.</span></span> <span data-ttu-id="e0b6c-307">Entrées avec plus d’importance affichera avant les entrées avec poids inférieur.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-307">Entries with higher weight will show before entries with lower weight.</span></span> <span data-ttu-id="e0b6c-308">La liste complète de saisie semi-automatique est triée par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-308">The complete autocomplete list is sorted by this property.</span></span> <span data-ttu-id="e0b6c-309">Le poids régulièrement diminue au fil du temps et augmente lorsque l’utilisateur envoie un message électronique à ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-309">The weight periodically decreases over time and increases when the user sends an email to this recipient.</span></span> <span data-ttu-id="e0b6c-310">Voir la description plus loin dans cette rubrique pour plus d’informations sur cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-310">See the description later in this topic for more information about this property.</span></span>  <br/> |
   
<span data-ttu-id="e0b6c-311">PR_NICK_NAME_WEIGHT</span><span class="sxs-lookup"><span data-stu-id="e0b6c-311">PR_NICK_NAME_WEIGHT</span></span>
  
<span data-ttu-id="e0b6c-312">Le jeu de lignes dans le flux de saisie semi-automatique est trié par ordre décroissant par la propriété PR_NICK_NAME_WEIGHT et le flux de saisie semi-automatique doit conserver toujours cette caractéristique triée.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-312">The set of rows in the autocomplete stream is sorted in descending order by the PR_NICK_NAME_WEIGHT property and the autocomplete stream should always preserve this sorted characteristic.</span></span> <span data-ttu-id="e0b6c-313">Par conséquent, toute modification apportée aux poids d’une ligne Assurez-vous également que position de la ligne conserve l’ordre de tri de l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-313">Therefore, any changes to a row's weight should also ensure that the row's position maintains the sorted order of the complete set of rows.</span></span> <span data-ttu-id="e0b6c-314">Les ajouts à l’ensemble de ligne doivent être insérés à la position correcte pour mettre à jour l’ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-314">Any additions to the row-set should be inserted to the correct position to maintain the sorted order.</span></span>
  
<span data-ttu-id="e0b6c-315">La valeur minimale de ce poids est 0 x 1 et la valeur maximale est LONG_MAX.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-315">The minimum value of this weight is 0x1 and the maximum value is LONG_MAX.</span></span> <span data-ttu-id="e0b6c-316">Toutes les autres valeurs de l’épaisseur sont considérés comme non valides.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-316">Any other values for the weight are considered invalid.</span></span>
  
<span data-ttu-id="e0b6c-317">Lorsque Outlook 2007 envoie un message à ou résout un destinataire, elle augmentera poids de ce destinataire 0 x 2000.</span><span class="sxs-lookup"><span data-stu-id="e0b6c-317">When Outlook 2007 sends a mail to or resolves a recipient, it will increase that recipient's weight by 0x2000.</span></span>
  

