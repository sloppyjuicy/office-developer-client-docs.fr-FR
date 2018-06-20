---
title: IProfAdminGetProfileTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetProfileTable
api_type:
- COM
ms.assetid: cebccd2d-8215-486e-9964-7fc42412cec6
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c942bdbf27590dde04b84970e345f265bc645045
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784385"
---
# <a name="iprofadmingetprofiletable"></a><span data-ttu-id="15db4-103">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="15db4-103">IProfAdmin::GetProfileTable</span></span>

  
  
<span data-ttu-id="15db4-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="15db4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="15db4-105">Permet d’accéder à la table de profil, un tableau qui contient des informations sur tous les profils disponibles.</span><span class="sxs-lookup"><span data-stu-id="15db4-105">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="15db4-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="15db4-106">Parameters</span></span>

 <span data-ttu-id="15db4-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="15db4-107">_ulFlags_</span></span>
  
> <span data-ttu-id="15db4-108">[in] Toujours NULL.</span><span class="sxs-lookup"><span data-stu-id="15db4-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="15db4-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="15db4-109">_lppTable_</span></span>
  
> <span data-ttu-id="15db4-110">[out] Pointeur vers un pointeur vers la table de profils.</span><span class="sxs-lookup"><span data-stu-id="15db4-110">[out] A pointer to a pointer to the profile table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="15db4-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="15db4-111">Return value</span></span>

<span data-ttu-id="15db4-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="15db4-112">S_OK</span></span> 
  
> <span data-ttu-id="15db4-113">Le tableau de profil a été récupéré correctement.</span><span class="sxs-lookup"><span data-stu-id="15db4-113">The profile table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="15db4-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="15db4-114">Remarks</span></span>

<span data-ttu-id="15db4-115">La méthode **IProfAdmin::GetProfileTable** permet d’accéder à la table de profil, qui contient une ligne pour chaque profil disponible.</span><span class="sxs-lookup"><span data-stu-id="15db4-115">The **IProfAdmin::GetProfileTable** method provides access to the profile table, which contains one row for every available profile.</span></span> <span data-ttu-id="15db4-116">Il existe deux colonnes dans chaque ligne : nom d’affichage du profil et d’un indicateur qui indique si le profil est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="15db4-116">There are only two columns in each row: the profile's display name, and a flag that indicates whether the profile is the default.</span></span> 
  
<span data-ttu-id="15db4-117">Profils qui ont été supprimés, ou qui ont été marquées pour suppression, mais qui sont en cours d’utilisation ne sont pas inclus dans la table de profils.</span><span class="sxs-lookup"><span data-stu-id="15db4-117">Profiles that have been deleted, or that are in use but have been marked for deletion, are not included in the profile table.</span></span> <span data-ttu-id="15db4-118">Le tableau de profil est statique ; les ajouts et suppressions de profils ne sont pas reflétées dans la table.</span><span class="sxs-lookup"><span data-stu-id="15db4-118">The profile table is static; subsequent additions and deletions of profiles are not reflected in the table.</span></span> 
  
<span data-ttu-id="15db4-119">Si aucun profil n’existe pas, **GetProfileTable** renvoie un tableau avec des lignes de zéro.</span><span class="sxs-lookup"><span data-stu-id="15db4-119">If no profiles exist, **GetProfileTable** returns a table with zero rows.</span></span> 
  
<span data-ttu-id="15db4-120">Pour plus d’informations sur la table de profils, voir [Les Tables de profil](profile-tables.md).</span><span class="sxs-lookup"><span data-stu-id="15db4-120">For more information about the profile table, see [Profile Tables](profile-tables.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="15db4-121">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="15db4-121">MFCMAPI reference</span></span>

<span data-ttu-id="15db4-122">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="15db4-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="15db4-123">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="15db4-123">**File**</span></span>|<span data-ttu-id="15db4-124">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="15db4-124">**Function**</span></span>|<span data-ttu-id="15db4-125">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="15db4-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="15db4-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="15db4-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="15db4-127">CMainDlg::OnShowProfiles</span><span class="sxs-lookup"><span data-stu-id="15db4-127">CMainDlg::OnShowProfiles</span></span>  <br/> |<span data-ttu-id="15db4-128">MFCMAPI utilise la méthode **IProfAdmin::GetProfileTable** pour obtenir le tableau de profil à afficher dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="15db4-128">MFCMAPI uses the **IProfAdmin::GetProfileTable** method to get the profile table to display in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="15db4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15db4-129">See also</span></span>



[<span data-ttu-id="15db4-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="15db4-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="15db4-131">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="15db4-131">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="15db4-132">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="15db4-132">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="15db4-133">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="15db4-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

