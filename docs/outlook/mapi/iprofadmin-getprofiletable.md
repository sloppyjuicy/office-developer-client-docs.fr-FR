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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2db7dba67e7b71df6921ecd97189255a0ef7823a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414644"
---
# <a name="iprofadmingetprofiletable"></a><span data-ttu-id="f9067-103">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="f9067-103">IProfAdmin::GetProfileTable</span></span>

  
  
<span data-ttu-id="f9067-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9067-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9067-105">Fournit l'accès à la table de profils, une table qui contient des informations sur tous les profils disponibles.</span><span class="sxs-lookup"><span data-stu-id="f9067-105">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="f9067-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9067-106">Parameters</span></span>

 <span data-ttu-id="f9067-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f9067-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f9067-108">dans Toujours NULL.</span><span class="sxs-lookup"><span data-stu-id="f9067-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="f9067-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="f9067-109">_lppTable_</span></span>
  
> <span data-ttu-id="f9067-110">remarquer Pointeur vers un pointeur vers le tableau de profils.</span><span class="sxs-lookup"><span data-stu-id="f9067-110">[out] A pointer to a pointer to the profile table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f9067-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f9067-111">Return value</span></span>

<span data-ttu-id="f9067-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="f9067-112">S_OK</span></span> 
  
> <span data-ttu-id="f9067-113">La table de profils a été correctement récupérée.</span><span class="sxs-lookup"><span data-stu-id="f9067-113">The profile table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f9067-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f9067-114">Remarks</span></span>

<span data-ttu-id="f9067-115">La méthode **IProfAdmin:: GetProfileTable** fournit l'accès à la table de profils, qui contient une ligne pour chaque profil disponible.</span><span class="sxs-lookup"><span data-stu-id="f9067-115">The **IProfAdmin::GetProfileTable** method provides access to the profile table, which contains one row for every available profile.</span></span> <span data-ttu-id="f9067-116">Chaque ligne comporte uniquement deux colonnes: le nom d'affichage du profil et un indicateur qui indique si le profil est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f9067-116">There are only two columns in each row: the profile's display name, and a flag that indicates whether the profile is the default.</span></span> 
  
<span data-ttu-id="f9067-117">Les profils qui ont été supprimés, ou qui sont en cours d'utilisation mais qui ont été marqués pour suppression, ne sont pas inclus dans la table de profils.</span><span class="sxs-lookup"><span data-stu-id="f9067-117">Profiles that have been deleted, or that are in use but have been marked for deletion, are not included in the profile table.</span></span> <span data-ttu-id="f9067-118">La table de profils est statique; les ajouts et suppressions de profils suivants ne sont pas répercutés dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="f9067-118">The profile table is static; subsequent additions and deletions of profiles are not reflected in the table.</span></span> 
  
<span data-ttu-id="f9067-119">Si aucun profil n'existe, **GetProfileTable** renvoie un tableau sans aucune ligne.</span><span class="sxs-lookup"><span data-stu-id="f9067-119">If no profiles exist, **GetProfileTable** returns a table with zero rows.</span></span> 
  
<span data-ttu-id="f9067-120">Pour plus d'informations sur la table de profils, voir [Profile tables](profile-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f9067-120">For more information about the profile table, see [Profile Tables](profile-tables.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f9067-121">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f9067-121">MFCMAPI reference</span></span>

<span data-ttu-id="f9067-122">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f9067-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f9067-123">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="f9067-123">**File**</span></span>|<span data-ttu-id="f9067-124">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="f9067-124">**Function**</span></span>|<span data-ttu-id="f9067-125">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="f9067-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f9067-126">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="f9067-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="f9067-127">CMainDlg:: OnShowProfiles</span><span class="sxs-lookup"><span data-stu-id="f9067-127">CMainDlg::OnShowProfiles</span></span>  <br/> |<span data-ttu-id="f9067-128">MFCMAPI utilise la méthode **IProfAdmin:: GetProfileTable** pour obtenir la table de profil à afficher dans une nouvelle boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f9067-128">MFCMAPI uses the **IProfAdmin::GetProfileTable** method to get the profile table to display in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f9067-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9067-129">See also</span></span>



[<span data-ttu-id="f9067-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f9067-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="f9067-131">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="f9067-131">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="f9067-132">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f9067-132">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="f9067-133">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="f9067-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

