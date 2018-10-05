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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389959"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a><span data-ttu-id="d7d7e-103">Propriété canonique PidTagFolderWebViewInfo</span><span class="sxs-lookup"><span data-stu-id="d7d7e-103">PidTagFolderWebViewInfo Cannonical Property</span></span>

  
  
<span data-ttu-id="d7d7e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7d7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7d7e-105">Contient l’URL de la page d’accueil d’un dossier dans Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-105">Contains the URL for the home page of a folder in Microsoft Outlook.</span></span> <span data-ttu-id="d7d7e-106">Cette propriété contient un flux binaire appelé **WebViewPersistenceObject**.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-106">This property contains a binary stream called **WebViewPersistenceObject**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7d7e-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d7d7e-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="d7d7e-108">PR_FOLDER_WEBVIEWINFO</span><span class="sxs-lookup"><span data-stu-id="d7d7e-108">PR_FOLDER_WEBVIEWINFO</span></span>  <br/> |
|<span data-ttu-id="d7d7e-109">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d7d7e-109">Identifier:</span></span>  <br/> |<span data-ttu-id="d7d7e-110">0x36DF</span><span class="sxs-lookup"><span data-stu-id="d7d7e-110">0x36DF</span></span>  <br/> |
|<span data-ttu-id="d7d7e-111">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d7d7e-111">Data type:</span></span>  <br/> |<span data-ttu-id="d7d7e-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d7d7e-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d7d7e-113">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d7d7e-113">Area:</span></span>  <br/> |<span data-ttu-id="d7d7e-114">Dossier MAPI</span><span class="sxs-lookup"><span data-stu-id="d7d7e-114">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7d7e-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="d7d7e-115">Remarks</span></span>

<span data-ttu-id="d7d7e-116">Une URL de page d’accueil peut être spécifiée pour n’importe quel dossier Outlook.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-116">A home page URL can be specified for any Outlook folder.</span></span> <span data-ttu-id="d7d7e-117">Ces informations sont accessibles dans Outlook à partir de l’onglet de la **Page d’accueil** de la boîte de dialogue Propriétés d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-117">This information can be accessed in Outlook from the **Home Page** tab of the Properties dialog box for a folder.</span></span> 
  
<span data-ttu-id="d7d7e-118">En fonction de certains paramètres de stratégie, la page d’accueil peut être ignorée par Outlook si la banque MAPI qui contient ce dossier ne signale pas MSCAP_SECURE_FOLDER_HOMEPAGES dans son implémentation [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="d7d7e-118">Depending on certain policy settings, the home page might be ignored by Outlook if the MAPI store that contains this folder does not report MSCAP_SECURE_FOLDER_HOMEPAGES in its [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) implementation.</span></span> 
  
<span data-ttu-id="d7d7e-119">Le dossier **Outlook aujourd'hui** et un dossier public peuvent avoir des URL de page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-119">Both the **Outlook Today** folder and a public folder can have home page URLs.</span></span> <span data-ttu-id="d7d7e-120">Toutefois le dossier **Outlook aujourd'hui** utilise un autre mécanisme pour gérer les URL de sa page d’accueil ; Ce mécanisme n’est pas couvertes dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-120">However the **Outlook Today** folder uses a different mechanism to manage its home page URL; that mechanism is not covered in this topic.</span></span> <span data-ttu-id="d7d7e-121">Un dossier public peut également avoir une URL de page d’accueil définie dans ce qui est spécifique à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-121">A public folder might also have a home page URL defined in it that is specific to a user.</span></span> <span data-ttu-id="d7d7e-122">Toutefois, cette fonctionnalité n’est pas décrite dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-122">However, that capability is not described in this topic.</span></span> 
  
<span data-ttu-id="d7d7e-123">La valeur de cette propriété est un flux binaire appelé **WebViewPersistenceObject**.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-123">The value of this property is a binary stream called **WebViewPersistenceObject**.</span></span>
  
### <a name="webviewpersistenceobject-stream-structure"></a><span data-ttu-id="d7d7e-124">Structure de flux WebViewPersistenceObject</span><span class="sxs-lookup"><span data-stu-id="d7d7e-124">WebViewPersistenceObject Stream Structure</span></span>

<span data-ttu-id="d7d7e-125">La structure de flux **WebViewPersistenceObject** contient des informations sur une URL de page d’accueil d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-125">The **WebViewPersistenceObject** stream structure contains information about a home page URL for a folder.</span></span> 
  
<span data-ttu-id="d7d7e-126">Éléments de données dans cette structure sont stockés dans l’ordre de primauté des octets, immédiatement après l’autre dans l’ordre suivant spécifié.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-126">Data elements in this structure are stored in little-endian byte order, immediately following one another in the following specified order.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d7d7e-127">La description suivante peut ne pas contenir toutes les valeurs de champ pris en charge par Outlook. Par conséquent, lorsque votre code lit un flux existant, des indicateurs qui ne sont pas répertoriés ici peuvent également se trouver.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-127">The following description may not list all of the field values supported by Outlook; therefore, when your code reads an existing stream, some flags that are not listed here might also be found.</span></span> <span data-ttu-id="d7d7e-128">Toutefois, vous pouvez utiliser cette description pour créer par programme des valeurs de la propriété **PidTagFolderWebViewInfo** maîtriser Outlook.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-128">However, you can use this description to programmatically create values for the **PidTagFolderWebViewInfo** property that Outlook will understand.</span></span> 
  
 <span data-ttu-id="d7d7e-129">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="d7d7e-129">_dwVersion_</span></span>
  
> <span data-ttu-id="d7d7e-130">Valeur DWORD (4 octets).</span><span class="sxs-lookup"><span data-stu-id="d7d7e-130">DWORD (4 bytes).</span></span> <span data-ttu-id="d7d7e-131">La version du format de la structure.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-131">The version of the structure's format.</span></span> <span data-ttu-id="d7d7e-132">Microsoft Office Outlook 2007, la seule valeur pris en charge pour ce champ est comme suit.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-132">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="d7d7e-133">**Nom de valeur**</span><span class="sxs-lookup"><span data-stu-id="d7d7e-133">**Value name**</span></span>|<span data-ttu-id="d7d7e-134">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="d7d7e-134">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d7d7e-135">WEBVIEW_PERSISTENCE_VERSION</span><span class="sxs-lookup"><span data-stu-id="d7d7e-135">WEBVIEW_PERSISTENCE_VERSION</span></span>  <br/> |<span data-ttu-id="d7d7e-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d7d7e-136">0x00000002</span></span>  <br/> |
   
 <span data-ttu-id="d7d7e-137">_dwType_</span><span class="sxs-lookup"><span data-stu-id="d7d7e-137">_dwType_</span></span>
  
> <span data-ttu-id="d7d7e-138">Valeur DWORD (4 octets).</span><span class="sxs-lookup"><span data-stu-id="d7d7e-138">DWORD (4 bytes).</span></span> <span data-ttu-id="d7d7e-139">Le type d’informations de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-139">The type of the home page information.</span></span> <span data-ttu-id="d7d7e-140">Microsoft Office Outlook 2007, la seule valeur pris en charge pour ce champ est comme suit.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-140">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="d7d7e-141">**Nom de valeur**</span><span class="sxs-lookup"><span data-stu-id="d7d7e-141">**Value name**</span></span>|<span data-ttu-id="d7d7e-142">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="d7d7e-142">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d7d7e-143">WEBVIEWURL</span><span class="sxs-lookup"><span data-stu-id="d7d7e-143">WEBVIEWURL</span></span>  <br/> |<span data-ttu-id="d7d7e-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d7d7e-144">0x00000001</span></span>  <br/> |
   
 <span data-ttu-id="d7d7e-145">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="d7d7e-145">_dwFlags_</span></span>
  
> <span data-ttu-id="d7d7e-146">Valeur DWORD (4 octets).</span><span class="sxs-lookup"><span data-stu-id="d7d7e-146">DWORD (4 bytes).</span></span> <span data-ttu-id="d7d7e-147">Une combinaison de zéro ou plusieurs indicateurs dont les valeurs et significations sont répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-147">A combination of zero or more flags whose values and meanings are listed in the following table.</span></span>
    
|<span data-ttu-id="d7d7e-148">Indicateur nom \*\*\*</span><span class="sxs-lookup"><span data-stu-id="d7d7e-148">\*\*\*\*Flag name\*\*\*\*</span></span>|<span data-ttu-id="d7d7e-149">\*\*\*\*Valeur\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d7d7e-149">\*\*\*\*Value\*\*\*\*</span></span>|<span data-ttu-id="d7d7e-150">\*\*\*\*Description\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d7d7e-150">\*\*\*\*Description\*\*\*\*</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d7d7e-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="d7d7e-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span></span>  <br/> |<span data-ttu-id="d7d7e-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d7d7e-152">0x00000001</span></span>  <br/> |<span data-ttu-id="d7d7e-153">La case à cocher **Afficher la page d’accueil par défaut pour ce dossier** a été activée dans l’onglet **Page d’accueil** de la boîte de dialogue Propriétés d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-153">The **Show home page by default for this folder** check box was checked in the **Home Page** tab of the Properties dialog box for a folder.</span></span>  <br/> |
   
 <span data-ttu-id="d7d7e-154">_dwUnused [7]_</span><span class="sxs-lookup"><span data-stu-id="d7d7e-154">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="d7d7e-155">Tableau 7 éléments DWORD (nombre total de 28 octets).</span><span class="sxs-lookup"><span data-stu-id="d7d7e-155">An array of 7 DWORD elements (28 bytes total).</span></span> <span data-ttu-id="d7d7e-156">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-156">Unused.</span></span>
    
<span data-ttu-id="d7d7e-157">cbData</span><span class="sxs-lookup"><span data-stu-id="d7d7e-157">cbData</span></span>
  
> <span data-ttu-id="d7d7e-158">ULONG (4 octets).</span><span class="sxs-lookup"><span data-stu-id="d7d7e-158">A ULONG (4 bytes).</span></span> <span data-ttu-id="d7d7e-159">La taille, en octets, de l’élément de données _wzURL_ .</span><span class="sxs-lookup"><span data-stu-id="d7d7e-159">The size, in bytes, of the  _wzURL_ data element.</span></span> 
    
 <span data-ttu-id="d7d7e-160">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="d7d7e-160">_wzURL_</span></span>
  
> <span data-ttu-id="d7d7e-161">Tableau d’éléments WCHAR.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-161">An array of WCHAR elements.</span></span> <span data-ttu-id="d7d7e-162">La représentation UTF-16 de la chaîne d’URL de page d’accueil se terminant par zéro.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-162">The UTF-16 representation of the zero-terminated home page URL string.</span></span>
    
### <a name="webviewpersistenceobject-stream-sample"></a><span data-ttu-id="d7d7e-163">Exemple de flux de données WebViewPersistenceObject</span><span class="sxs-lookup"><span data-stu-id="d7d7e-163">WebViewPersistenceObject Stream Sample</span></span>

<span data-ttu-id="d7d7e-164">Cette section décrit un exemple d’un flux **WebViewPersistenceObject** .</span><span class="sxs-lookup"><span data-stu-id="d7d7e-164">This section describes an example of a **WebViewPersistenceObject** stream.</span></span> <span data-ttu-id="d7d7e-165">Le flux Spécifie l’URL de la page d’accueil «https://www.microsoft.com».</span><span class="sxs-lookup"><span data-stu-id="d7d7e-165">The stream specifies the home page URL "https://www.microsoft.com".</span></span> 
  
 <span data-ttu-id="d7d7e-166">**Vidage des données**</span><span class="sxs-lookup"><span data-stu-id="d7d7e-166">**Data dump**</span></span>
  
<span data-ttu-id="d7d7e-167">Vous trouverez ci-dessous un vidage des données de l’objet stream tel qu’il doit être affiché dans un éditeur binaire.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-167">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="d7d7e-168">**Décalage de flux**</span><span class="sxs-lookup"><span data-stu-id="d7d7e-168">**Stream offset**</span></span>|<span data-ttu-id="d7d7e-169">**Octets de données**</span><span class="sxs-lookup"><span data-stu-id="d7d7e-169">**Data bytes**</span></span>|<span data-ttu-id="d7d7e-170">**Données ASCII**</span><span class="sxs-lookup"><span data-stu-id="d7d7e-170">**ASCII data**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d7d7e-171">0000000000</span><span class="sxs-lookup"><span data-stu-id="d7d7e-171">0000000000</span></span>  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|<span data-ttu-id="d7d7e-172">0000000010</span><span class="sxs-lookup"><span data-stu-id="d7d7e-172">0000000010</span></span>  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|<span data-ttu-id="d7d7e-173">0000000020</span><span class="sxs-lookup"><span data-stu-id="d7d7e-173">0000000020</span></span>  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|<span data-ttu-id="d7d7e-174">0000000030</span><span class="sxs-lookup"><span data-stu-id="d7d7e-174">0000000030</span></span>  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|<span data-ttu-id="d7d7e-175">0000000040</span><span class="sxs-lookup"><span data-stu-id="d7d7e-175">0000000040</span></span>  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|<span data-ttu-id="d7d7e-176">0000000050</span><span class="sxs-lookup"><span data-stu-id="d7d7e-176">0000000050</span></span>  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
<span data-ttu-id="d7d7e-177">Vous trouverez ci-dessous une analyse des données pour le flux **WebViewPersistenceObject** .</span><span class="sxs-lookup"><span data-stu-id="d7d7e-177">The following is a parse of the sample data for the **WebViewPersistenceObject** stream.</span></span> 
  
 <span data-ttu-id="d7d7e-178">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="d7d7e-178">_dwVersion_</span></span>
  
> <span data-ttu-id="d7d7e-179">Décalage de 0 x 0, 4 octets : 0 x 00000002 (WEBVIEW_PERSISTENCE_VERSION).</span><span class="sxs-lookup"><span data-stu-id="d7d7e-179">Offset 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span></span>
    
 <span data-ttu-id="d7d7e-180">_dwType_</span><span class="sxs-lookup"><span data-stu-id="d7d7e-180">_dwType_</span></span>
  
> <span data-ttu-id="d7d7e-181">Décalage de 0 x 4, 4 octets : 0 x 00000001 (WEBVIEWURL).</span><span class="sxs-lookup"><span data-stu-id="d7d7e-181">Offset 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).</span></span>
    
 <span data-ttu-id="d7d7e-182">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="d7d7e-182">_dwFlags_</span></span>
  
> <span data-ttu-id="d7d7e-183">Décalage de 0 x 8, 4 octets : 0 x 00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span><span class="sxs-lookup"><span data-stu-id="d7d7e-183">Offset 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span></span>
    
 <span data-ttu-id="d7d7e-184">_dwUnused [7]_</span><span class="sxs-lookup"><span data-stu-id="d7d7e-184">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="d7d7e-185">Décalage 0xC, 28 octets : tous les zéros.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-185">Offset 0xC, 28 bytes: all zeros.</span></span>
    
 <span data-ttu-id="d7d7e-186">_cbData_</span><span class="sxs-lookup"><span data-stu-id="d7d7e-186">_cbData_</span></span>
  
> <span data-ttu-id="d7d7e-187">Décalage de 0 x 28, 4 octets : 0 x 00000032.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-187">Offset 0x28, 4 bytes: 0x00000032.</span></span>
    
 <span data-ttu-id="d7d7e-188">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="d7d7e-188">_wzURL_</span></span>
  
> <span data-ttu-id="d7d7e-189">Décalage 0x2C, 0 x 32 octets : tableau de 25 WCHAR.</span><span class="sxs-lookup"><span data-stu-id="d7d7e-189">Offset 0x2C, 0x32 bytes: array of 25 WCHARs.</span></span> <span data-ttu-id="d7d7e-190">Une valeur de chaîne terminée par zéro Unicode : «https://www.microsoft.com».</span><span class="sxs-lookup"><span data-stu-id="d7d7e-190">A Unicode zero-terminated string value: "https://www.microsoft.com".</span></span>
    

