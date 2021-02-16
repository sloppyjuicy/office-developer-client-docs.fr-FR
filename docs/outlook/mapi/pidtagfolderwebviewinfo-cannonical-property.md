---
title: Propriété canonique PidTagFolderWebViewInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderWebViewInfo
api_type:
- HeaderDef
ms.assetid: 96ea23df-aa4f-4b3e-9663-e7db39f668c1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 70932e703511235e9f5e32efd95b18d1b66494e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316309"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a><span data-ttu-id="bce1d-103">Propriété canonique PidTagFolderWebViewInfo</span><span class="sxs-lookup"><span data-stu-id="bce1d-103">PidTagFolderWebViewInfo Cannonical Property</span></span>

  
  
<span data-ttu-id="bce1d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bce1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bce1d-105">Contient l’URL de la page d’accueil d’un dossier dans Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="bce1d-105">Contains the URL for the home page of a folder in Microsoft Outlook.</span></span> <span data-ttu-id="bce1d-106">Cette propriété contient un flux binaire appelé **WebViewPersistenceObject**.</span><span class="sxs-lookup"><span data-stu-id="bce1d-106">This property contains a binary stream called **WebViewPersistenceObject**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bce1d-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="bce1d-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="bce1d-108">PR_FOLDER_WEBVIEWINFO</span><span class="sxs-lookup"><span data-stu-id="bce1d-108">PR_FOLDER_WEBVIEWINFO</span></span>  <br/> |
|<span data-ttu-id="bce1d-109">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="bce1d-109">Identifier:</span></span>  <br/> |<span data-ttu-id="bce1d-110">0x36DF</span><span class="sxs-lookup"><span data-stu-id="bce1d-110">0x36DF</span></span>  <br/> |
|<span data-ttu-id="bce1d-111">Type de données :</span><span class="sxs-lookup"><span data-stu-id="bce1d-111">Data type:</span></span>  <br/> |<span data-ttu-id="bce1d-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bce1d-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bce1d-113">Domaine :</span><span class="sxs-lookup"><span data-stu-id="bce1d-113">Area:</span></span>  <br/> |<span data-ttu-id="bce1d-114">Dossier MAPI</span><span class="sxs-lookup"><span data-stu-id="bce1d-114">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bce1d-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="bce1d-115">Remarks</span></span>

<span data-ttu-id="bce1d-116">Une URL de page d’accueil peut être spécifiée pour n’importe quel dossier Outlook.</span><span class="sxs-lookup"><span data-stu-id="bce1d-116">A home page URL can be specified for any Outlook folder.</span></span> <span data-ttu-id="bce1d-117">Ces informations sont accessibles dans Outlook à partir de l’onglet **Page** d’accueil de la boîte de dialogue Propriétés d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="bce1d-117">This information can be accessed in Outlook from the **Home Page** tab of the Properties dialog box for a folder.</span></span> 
  
<span data-ttu-id="bce1d-118">Selon certains paramètres de stratégie, la page d’accueil peut être ignorée par Outlook si le magasin MAPI qui contient ce dossier ne signale pas MSCAP_SECURE_FOLDER_HOMEPAGES dans son implémentation [IMSCapabilities::GetCapabilities.](pidtagfolderwebviewinfo-cannonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="bce1d-118">Depending on certain policy settings, the home page might be ignored by Outlook if the MAPI store that contains this folder does not report MSCAP_SECURE_FOLDER_HOMEPAGES in its [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) implementation.</span></span> 
  
<span data-ttu-id="bce1d-119">Le dossier **Outlook Today** et un dossier public peuvent avoir des URL de page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="bce1d-119">Both the **Outlook Today** folder and a public folder can have home page URLs.</span></span> <span data-ttu-id="bce1d-120">Toutefois, **le dossier Outlook Today** utilise un mécanisme différent pour gérer l’URL de sa page d’accueil . ce mécanisme n’est pas abordé dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="bce1d-120">However the **Outlook Today** folder uses a different mechanism to manage its home page URL; that mechanism is not covered in this topic.</span></span> <span data-ttu-id="bce1d-121">Une URL de page d’accueil spécifique à un utilisateur peut également être définie dans un dossier public.</span><span class="sxs-lookup"><span data-stu-id="bce1d-121">A public folder might also have a home page URL defined in it that is specific to a user.</span></span> <span data-ttu-id="bce1d-122">Toutefois, cette fonctionnalité n’est pas décrite dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="bce1d-122">However, that capability is not described in this topic.</span></span> 
  
<span data-ttu-id="bce1d-123">La valeur de cette propriété est un flux binaire appelé **WebViewPersistenceObject**.</span><span class="sxs-lookup"><span data-stu-id="bce1d-123">The value of this property is a binary stream called **WebViewPersistenceObject**.</span></span>
  
### <a name="webviewpersistenceobject-stream-structure"></a><span data-ttu-id="bce1d-124">Structure de flux WebViewPersistenceObject</span><span class="sxs-lookup"><span data-stu-id="bce1d-124">WebViewPersistenceObject Stream Structure</span></span>

<span data-ttu-id="bce1d-125">La structure **de flux WebViewPersistenceObject** contient des informations sur une URL de page d’accueil pour un dossier.</span><span class="sxs-lookup"><span data-stu-id="bce1d-125">The **WebViewPersistenceObject** stream structure contains information about a home page URL for a folder.</span></span> 
  
<span data-ttu-id="bce1d-126">Les éléments de données de cette structure sont stockés dans l’ordre des petits bouts, immédiatement après les autres dans l’ordre spécifié suivant.</span><span class="sxs-lookup"><span data-stu-id="bce1d-126">Data elements in this structure are stored in little-endian byte order, immediately following one another in the following specified order.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bce1d-127">La description suivante peut ne pas lister toutes les valeurs de champ pris en charge par Outlook ; par conséquent, lorsque votre code lit un flux existant, certains indicateurs qui ne sont pas répertoriés ici peuvent également être trouvés.</span><span class="sxs-lookup"><span data-stu-id="bce1d-127">The following description may not list all of the field values supported by Outlook; therefore, when your code reads an existing stream, some flags that are not listed here might also be found.</span></span> <span data-ttu-id="bce1d-128">Toutefois, vous pouvez utiliser cette description pour créer par programme des valeurs pour la **propriété PidTagFolderWebViewInfo** qu’Outlook comprendra.</span><span class="sxs-lookup"><span data-stu-id="bce1d-128">However, you can use this description to programmatically create values for the **PidTagFolderWebViewInfo** property that Outlook will understand.</span></span> 
  
 <span data-ttu-id="bce1d-129">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="bce1d-129">_dwVersion_</span></span>
  
> <span data-ttu-id="bce1d-130">DWORD (4 octets).</span><span class="sxs-lookup"><span data-stu-id="bce1d-130">DWORD (4 bytes).</span></span> <span data-ttu-id="bce1d-131">Version du format de la structure.</span><span class="sxs-lookup"><span data-stu-id="bce1d-131">The version of the structure's format.</span></span> <span data-ttu-id="bce1d-132">À partir Microsoft Office Outlook 2007, la seule valeur prise en charge pour ce champ est la suivante.</span><span class="sxs-lookup"><span data-stu-id="bce1d-132">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="bce1d-133">**Nom de la valeur**</span><span class="sxs-lookup"><span data-stu-id="bce1d-133">**Value name**</span></span>|<span data-ttu-id="bce1d-134">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="bce1d-134">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bce1d-135">WEBVIEW_PERSISTENCE_VERSION</span><span class="sxs-lookup"><span data-stu-id="bce1d-135">WEBVIEW_PERSISTENCE_VERSION</span></span>  <br/> |<span data-ttu-id="bce1d-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="bce1d-136">0x00000002</span></span>  <br/> |
   
 <span data-ttu-id="bce1d-137">_dwType_</span><span class="sxs-lookup"><span data-stu-id="bce1d-137">_dwType_</span></span>
  
> <span data-ttu-id="bce1d-138">DWORD (4 octets).</span><span class="sxs-lookup"><span data-stu-id="bce1d-138">DWORD (4 bytes).</span></span> <span data-ttu-id="bce1d-139">Type des informations de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="bce1d-139">The type of the home page information.</span></span> <span data-ttu-id="bce1d-140">À partir Microsoft Office Outlook 2007, la seule valeur prise en charge pour ce champ est la suivante.</span><span class="sxs-lookup"><span data-stu-id="bce1d-140">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="bce1d-141">**Nom de la valeur**</span><span class="sxs-lookup"><span data-stu-id="bce1d-141">**Value name**</span></span>|<span data-ttu-id="bce1d-142">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="bce1d-142">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bce1d-143">WEBVIEWURL</span><span class="sxs-lookup"><span data-stu-id="bce1d-143">WEBVIEWURL</span></span>  <br/> |<span data-ttu-id="bce1d-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bce1d-144">0x00000001</span></span>  <br/> |
   
 <span data-ttu-id="bce1d-145">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="bce1d-145">_dwFlags_</span></span>
  
> <span data-ttu-id="bce1d-146">DWORD (4 octets).</span><span class="sxs-lookup"><span data-stu-id="bce1d-146">DWORD (4 bytes).</span></span> <span data-ttu-id="bce1d-147">Combinaison de zéro ou plus d’indicateurs dont les valeurs et les significations sont répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="bce1d-147">A combination of zero or more flags whose values and meanings are listed in the following table.</span></span>
    
|<span data-ttu-id="bce1d-148">Nom de l’indicateur\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="bce1d-148">\*\*\*\*Flag name\*\*\*\*</span></span>|<span data-ttu-id="bce1d-149">\*\*\*\*Valeur\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="bce1d-149">\*\*\*\*Value\*\*\*\*</span></span>|<span data-ttu-id="bce1d-150">\*\*\*\*Description\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="bce1d-150">\*\*\*\*Description\*\*\*\*</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bce1d-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="bce1d-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span></span>  <br/> |<span data-ttu-id="bce1d-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bce1d-152">0x00000001</span></span>  <br/> |<span data-ttu-id="bce1d-153">La case à cocher Afficher **la page** d’accueil par défaut pour ce dossier a été cochée dans l’onglet **Page** d’accueil de la boîte de dialogue Propriétés d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="bce1d-153">The **Show home page by default for this folder** check box was checked in the **Home Page** tab of the Properties dialog box for a folder.</span></span>  <br/> |
   
 <span data-ttu-id="bce1d-154">_dwUnused[7]_</span><span class="sxs-lookup"><span data-stu-id="bce1d-154">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="bce1d-155">Tableau de 7 éléments DWORD (28 octets au total).</span><span class="sxs-lookup"><span data-stu-id="bce1d-155">An array of 7 DWORD elements (28 bytes total).</span></span> <span data-ttu-id="bce1d-156">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="bce1d-156">Unused.</span></span>
    
<span data-ttu-id="bce1d-157">cbData</span><span class="sxs-lookup"><span data-stu-id="bce1d-157">cbData</span></span>
  
> <span data-ttu-id="bce1d-158">ULONG (4 octets).</span><span class="sxs-lookup"><span data-stu-id="bce1d-158">A ULONG (4 bytes).</span></span> <span data-ttu-id="bce1d-159">Taille, en octets, de l’élément _de données wzURL._</span><span class="sxs-lookup"><span data-stu-id="bce1d-159">The size, in bytes, of the  _wzURL_ data element.</span></span> 
    
 <span data-ttu-id="bce1d-160">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="bce1d-160">_wzURL_</span></span>
  
> <span data-ttu-id="bce1d-161">Tableau d’éléments WCHAR.</span><span class="sxs-lookup"><span data-stu-id="bce1d-161">An array of WCHAR elements.</span></span> <span data-ttu-id="bce1d-162">Représentation UTF-16 de la chaîne d’URL de page d’accueil sans fin.</span><span class="sxs-lookup"><span data-stu-id="bce1d-162">The UTF-16 representation of the zero-terminated home page URL string.</span></span>
    
### <a name="webviewpersistenceobject-stream-sample"></a><span data-ttu-id="bce1d-163">Exemple de flux WebViewPersistenceObject</span><span class="sxs-lookup"><span data-stu-id="bce1d-163">WebViewPersistenceObject Stream Sample</span></span>

<span data-ttu-id="bce1d-164">Cette section décrit un exemple de **flux WebViewPersistenceObject.**</span><span class="sxs-lookup"><span data-stu-id="bce1d-164">This section describes an example of a **WebViewPersistenceObject** stream.</span></span> <span data-ttu-id="bce1d-165">Le flux spécifie l’URL de la page d’accueil « https://www.microsoft.com ».</span><span class="sxs-lookup"><span data-stu-id="bce1d-165">The stream specifies the home page URL "https://www.microsoft.com".</span></span> 
  
 <span data-ttu-id="bce1d-166">**Vidage de données**</span><span class="sxs-lookup"><span data-stu-id="bce1d-166">**Data dump**</span></span>
  
<span data-ttu-id="bce1d-167">Voici un vidage de données du flux tel qu’il serait affiché dans un éditeur binaire.</span><span class="sxs-lookup"><span data-stu-id="bce1d-167">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="bce1d-168">**Décalage de flux**</span><span class="sxs-lookup"><span data-stu-id="bce1d-168">**Stream offset**</span></span>|<span data-ttu-id="bce1d-169">**Octets de données**</span><span class="sxs-lookup"><span data-stu-id="bce1d-169">**Data bytes**</span></span>|<span data-ttu-id="bce1d-170">**Données ASCII**</span><span class="sxs-lookup"><span data-stu-id="bce1d-170">**ASCII data**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bce1d-171">0000000000</span><span class="sxs-lookup"><span data-stu-id="bce1d-171">0000000000</span></span>  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|<span data-ttu-id="bce1d-172">0000000010</span><span class="sxs-lookup"><span data-stu-id="bce1d-172">0000000010</span></span>  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|<span data-ttu-id="bce1d-173">0000000020</span><span class="sxs-lookup"><span data-stu-id="bce1d-173">0000000020</span></span>  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|<span data-ttu-id="bce1d-174">0000000030</span><span class="sxs-lookup"><span data-stu-id="bce1d-174">0000000030</span></span>  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|<span data-ttu-id="bce1d-175">0000000040</span><span class="sxs-lookup"><span data-stu-id="bce1d-175">0000000040</span></span>  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|<span data-ttu-id="bce1d-176">0000000050</span><span class="sxs-lookup"><span data-stu-id="bce1d-176">0000000050</span></span>  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
<span data-ttu-id="bce1d-177">Voici une analyse des exemples de données pour le **flux WebViewPersistenceObject.**</span><span class="sxs-lookup"><span data-stu-id="bce1d-177">The following is a parse of the sample data for the **WebViewPersistenceObject** stream.</span></span> 
  
 <span data-ttu-id="bce1d-178">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="bce1d-178">_dwVersion_</span></span>
  
> <span data-ttu-id="bce1d-179">Décalage 0x0, 4 octets : 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span><span class="sxs-lookup"><span data-stu-id="bce1d-179">Offset 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span></span>
    
 <span data-ttu-id="bce1d-180">_dwType_</span><span class="sxs-lookup"><span data-stu-id="bce1d-180">_dwType_</span></span>
  
> <span data-ttu-id="bce1d-181">Décalage 0x4, 4 octets : 0x00000001 (WEBVIEWURL).</span><span class="sxs-lookup"><span data-stu-id="bce1d-181">Offset 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).</span></span>
    
 <span data-ttu-id="bce1d-182">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="bce1d-182">_dwFlags_</span></span>
  
> <span data-ttu-id="bce1d-183">Décalage 0x8, 4 octets : 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span><span class="sxs-lookup"><span data-stu-id="bce1d-183">Offset 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span></span>
    
 <span data-ttu-id="bce1d-184">_dwUnused[7]_</span><span class="sxs-lookup"><span data-stu-id="bce1d-184">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="bce1d-185">Décalage 0xC, 28 octets : tous les zéros.</span><span class="sxs-lookup"><span data-stu-id="bce1d-185">Offset 0xC, 28 bytes: all zeros.</span></span>
    
 <span data-ttu-id="bce1d-186">_cbData_</span><span class="sxs-lookup"><span data-stu-id="bce1d-186">_cbData_</span></span>
  
> <span data-ttu-id="bce1d-187">Décalage 0x28, 4 octets : 0x00000032.</span><span class="sxs-lookup"><span data-stu-id="bce1d-187">Offset 0x28, 4 bytes: 0x00000032.</span></span>
    
 <span data-ttu-id="bce1d-188">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="bce1d-188">_wzURL_</span></span>
  
> <span data-ttu-id="bce1d-189">Décalage 0x2C, 0x32 octets : tableau de 25 WCHAR.</span><span class="sxs-lookup"><span data-stu-id="bce1d-189">Offset 0x2C, 0x32 bytes: array of 25 WCHARs.</span></span> <span data-ttu-id="bce1d-190">Valeur de chaîne Unicode sans fin : " https://www.microsoft.com « .</span><span class="sxs-lookup"><span data-stu-id="bce1d-190">A Unicode zero-terminated string value: "https://www.microsoft.com".</span></span>
    

