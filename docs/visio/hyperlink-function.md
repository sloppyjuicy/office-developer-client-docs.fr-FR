---
title: HYPERLINK, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251441
localization_priority: Normal
ms.assetid: 943636a6-e135-a626-7924-11e238156548
description: Permet d’accéder à l’adresse spécifiée, qui peut être un fichier, un unc ou un chemin d’URL.
ms.openlocfilehash: 5e4952c3d56eff0cb1e6518928a7b8259f645046
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329945"
---
# <a name="hyperlink-function"></a><span data-ttu-id="66716-103">Fonction HYPERLINK</span><span class="sxs-lookup"><span data-stu-id="66716-103">HYPERLINK Function</span></span>

<span data-ttu-id="66716-104">Permet d’accéder à l’adresse spécifiée, qui peut être un fichier, un unc ou un chemin d’URL.</span><span class="sxs-lookup"><span data-stu-id="66716-104">Navigates to the specified address, which can be a file, UNC, or URL path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="66716-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66716-105">Syntax</span></span>

<span data-ttu-id="66716-106">HYPERLINK( » \*\* *address* \*\* « [, » \*\* *subaddress* \*\* « , » \*\* *extrainfo* \*\* « , \*\* *window* \*\*, » \*\* *frame* \*\* « ])</span><span class="sxs-lookup"><span data-stu-id="66716-106">HYPERLINK(" \*\* *address* \*\* "[," \*\* *subaddress* \*\* "," \*\* *extrainfo* \*\* ", \*\* *window* \*\*," \*\* *frame* \*\* "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="66716-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66716-107">Parameters</span></span>

|<span data-ttu-id="66716-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="66716-108">**Name**</span></span>|<span data-ttu-id="66716-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="66716-109">**Required/Optional**</span></span>|<span data-ttu-id="66716-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="66716-110">**Data Type**</span></span>|<span data-ttu-id="66716-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="66716-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="66716-112">_adresse_</span><span class="sxs-lookup"><span data-stu-id="66716-112">_address_</span></span> <br/> |<span data-ttu-id="66716-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="66716-113">Required</span></span>  <br/> |<span data-ttu-id="66716-114">**String**</span><span class="sxs-lookup"><span data-stu-id="66716-114">**String**</span></span> <br/> |<span data-ttu-id="66716-115">Chemin d’accès complet ou relatif.</span><span class="sxs-lookup"><span data-stu-id="66716-115">A full path or a relative path.</span></span>  <br/> |
| <span data-ttu-id="66716-116">_sous-adresse_</span><span class="sxs-lookup"><span data-stu-id="66716-116">_subaddress_</span></span> <br/> |<span data-ttu-id="66716-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="66716-117">Optional</span></span>  <br/> |<span data-ttu-id="66716-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="66716-118">**String**</span></span> <br/> |<span data-ttu-id="66716-p101">Spécifie un emplacement dans address auquel se lier. Par exemple, si address est un fichier Microsoft Visio, subaddress peut être un nom de page. S’il s’agit d’un fichier Microsoft Excel, subaddress peut être une feuille de calcul ou une plage d’une feuille de calcul. Dans le cas d’une URL permettant d’accéder à une page HTML, subaddress peut être un point d’ancrage.</span><span class="sxs-lookup"><span data-stu-id="66716-p101">Specifies a location within address to link to. For example, if address is a Microsoft Visio file, subaddress can be a page name; if a Microsoft Excel file, subaddress can be a worksheet or range within a worksheet; if a URL for an HTML page, subaddress can be an anchor.</span></span>  <br/> |
| <span data-ttu-id="66716-121">_extrainfo_</span><span class="sxs-lookup"><span data-stu-id="66716-121">_extrainfo_</span></span> <br/> |<span data-ttu-id="66716-122">Facultatif</span><span class="sxs-lookup"><span data-stu-id="66716-122">Optional</span></span>  <br/> |<span data-ttu-id="66716-123">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="66716-123">**String**</span></span> <br/> |<span data-ttu-id="66716-124">Transmet les informations utilisées pour la résolution de l’URL, comme les coordonnées d’une image interactive.</span><span class="sxs-lookup"><span data-stu-id="66716-124">Passes information used in resolving the URL, such as the coordinates of an image map.</span></span>  <br/> |
| <span data-ttu-id="66716-125">_window_</span><span class="sxs-lookup"><span data-stu-id="66716-125">_window_</span></span> <br/> |<span data-ttu-id="66716-126">Facultatif</span><span class="sxs-lookup"><span data-stu-id="66716-126">Optional</span></span>  <br/> |<span data-ttu-id="66716-127">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="66716-127">**Boolean**</span></span> <br/> |<span data-ttu-id="66716-p102">Indique si le lien hypertexte s’ouvre dans une nouvelle fenêtre. La valeur par défaut est FALSE.</span><span class="sxs-lookup"><span data-stu-id="66716-p102">Specifies whether the hyperlink is opened in a new window. The default value is FALSE.</span></span>  <br/> |
| <span data-ttu-id="66716-130">_frame_</span><span class="sxs-lookup"><span data-stu-id="66716-130">_frame_</span></span> <br/> |<span data-ttu-id="66716-131">Facultatif</span><span class="sxs-lookup"><span data-stu-id="66716-131">Optional</span></span>  <br/> |<span data-ttu-id="66716-132">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="66716-132">**String**</span></span> <br/> | <span data-ttu-id="66716-p103">Spécifie le nom d’un cadre à cibler lorsque Visio est ouvert comme document ActiveX dans un navigateur ActiveX, tel que Microsoft Internet Explorer 3.0 ou ultérieur. Par défaut, cette chaîne est vide.</span><span class="sxs-lookup"><span data-stu-id="66716-p103">Specifies the name of a frame to target when Visio is open as an Active document in an ActiveX browser, such as Microsoft Internet Explorer 3.0 or later. The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66716-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="66716-135">Remarks</span></span>

<span data-ttu-id="66716-p104">Si le document n’est pas associé à un chemin d’accès de base, Visio navigue selon le chemin d’accès du document. Si le document n’a pas été enregistré, le lien hypertexte n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="66716-p104">If the document has no base path, Visio navigates according to the document path. If the document has not been saved, the hyperlink is undefined.</span></span> 
  
<span data-ttu-id="66716-138">Les chemins d’accès relatifs sont basés sur le champ **Répertoire Web** spécifié dans la boîte de dialogue **Propriétés Visio**.</span><span class="sxs-lookup"><span data-stu-id="66716-138">Relative paths are based on the **Hyperlink base** field specified in the **Visio Properties** dialog box.</span></span> 
  
<span data-ttu-id="66716-139">Vous pouvez utiliser la fonction GOTOPAGE pour naviguer vers différentes pages d’un document.</span><span class="sxs-lookup"><span data-stu-id="66716-139">You can use the GOTOPAGE function to navigate to pages of a document.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="66716-140">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="66716-140">Example 1</span></span>

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a><span data-ttu-id="66716-141">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="66716-141">Example 2</span></span>

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a><span data-ttu-id="66716-142">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="66716-142">Example 3</span></span>

 `HYPERLINK("https://www.microsoft.com")`
  
## <a name="example-4"></a><span data-ttu-id="66716-143">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="66716-143">Example 4</span></span>

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

