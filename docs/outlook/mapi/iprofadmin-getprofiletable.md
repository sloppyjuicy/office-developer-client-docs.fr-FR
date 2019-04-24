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
ms.openlocfilehash: 2db7dba67e7b71df6921ecd97189255a0ef7823a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309547"
---
# <a name="iprofadmingetprofiletable"></a><span data-ttu-id="5febe-103">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="5febe-103">IProfAdmin::GetProfileTable</span></span>

  
  
<span data-ttu-id="5febe-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5febe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5febe-105">Fournit l'accès à la table de profils, une table qui contient des informations sur tous les profils disponibles.</span><span class="sxs-lookup"><span data-stu-id="5febe-105">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="5febe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5febe-106">Parameters</span></span>

 <span data-ttu-id="5febe-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5febe-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5febe-108">dans Toujours NULL.</span><span class="sxs-lookup"><span data-stu-id="5febe-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="5febe-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="5febe-109">_lppTable_</span></span>
  
> <span data-ttu-id="5febe-110">remarquer Pointeur vers un pointeur vers le tableau de profils.</span><span class="sxs-lookup"><span data-stu-id="5febe-110">[out] A pointer to a pointer to the profile table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5febe-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5febe-111">Return value</span></span>

<span data-ttu-id="5febe-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="5febe-112">S_OK</span></span> 
  
> <span data-ttu-id="5febe-113">La table de profils a été correctement récupérée.</span><span class="sxs-lookup"><span data-stu-id="5febe-113">The profile table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5febe-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5febe-114">Remarks</span></span>

<span data-ttu-id="5febe-115">La méthode **IProfAdmin:: GetProfileTable** fournit l'accès à la table de profils, qui contient une ligne pour chaque profil disponible.</span><span class="sxs-lookup"><span data-stu-id="5febe-115">The **IProfAdmin::GetProfileTable** method provides access to the profile table, which contains one row for every available profile.</span></span> <span data-ttu-id="5febe-116">Chaque ligne comporte uniquement deux colonnes: le nom d'affichage du profil et un indicateur qui indique si le profil est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="5febe-116">There are only two columns in each row: the profile's display name, and a flag that indicates whether the profile is the default.</span></span> 
  
<span data-ttu-id="5febe-117">Les profils qui ont été supprimés, ou qui sont en cours d'utilisation mais qui ont été marqués pour suppression, ne sont pas inclus dans la table de profils.</span><span class="sxs-lookup"><span data-stu-id="5febe-117">Profiles that have been deleted, or that are in use but have been marked for deletion, are not included in the profile table.</span></span> <span data-ttu-id="5febe-118">La table de profils est statique; les ajouts et suppressions de profils suivants ne sont pas répercutés dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="5febe-118">The profile table is static; subsequent additions and deletions of profiles are not reflected in the table.</span></span> 
  
<span data-ttu-id="5febe-119">Si aucun profil n'existe, **GetProfileTable** renvoie un tableau sans aucune ligne.</span><span class="sxs-lookup"><span data-stu-id="5febe-119">If no profiles exist, **GetProfileTable** returns a table with zero rows.</span></span> 
  
<span data-ttu-id="5febe-120">Pour plus d'informations sur la table de profils, voir [Profile tables](profile-tables.md).</span><span class="sxs-lookup"><span data-stu-id="5febe-120">For more information about the profile table, see [Profile Tables](profile-tables.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5febe-121">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5febe-121">MFCMAPI reference</span></span>

<span data-ttu-id="5febe-122">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5febe-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5febe-123">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="5febe-123">**File**</span></span>|<span data-ttu-id="5febe-124">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="5febe-124">**Function**</span></span>|<span data-ttu-id="5febe-125">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="5febe-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5febe-126">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="5febe-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="5febe-127">CMainDlg:: OnShowProfiles</span><span class="sxs-lookup"><span data-stu-id="5febe-127">CMainDlg::OnShowProfiles</span></span>  <br/> |<span data-ttu-id="5febe-128">MFCMAPI utilise la méthode **IProfAdmin:: GetProfileTable** pour obtenir la table de profil à afficher dans une nouvelle boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="5febe-128">MFCMAPI uses the **IProfAdmin::GetProfileTable** method to get the profile table to display in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5febe-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5febe-129">See also</span></span>



[<span data-ttu-id="5febe-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5febe-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="5febe-131">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="5febe-131">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="5febe-132">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5febe-132">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="5febe-133">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="5febe-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

