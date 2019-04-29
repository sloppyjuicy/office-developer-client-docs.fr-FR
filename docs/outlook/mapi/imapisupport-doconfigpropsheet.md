---
title: IMAPISupportDoConfigPropsheet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoConfigPropsheet
api_type:
- COM
ms.assetid: 3899c49c-a0ec-4dca-92e8-e801cd4908cf
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: cd8727104af694d456074614b5ea7c222c9b91b9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429013"
---
# <a name="imapisupportdoconfigpropsheet"></a><span data-ttu-id="c9a3d-103">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="c9a3d-103">IMAPISupport::DoConfigPropsheet</span></span>

  
  
<span data-ttu-id="c9a3d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9a3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9a3d-105">Affiche une feuille de propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="c9a3d-105">Displays a configuration property sheet.</span></span>
  
```cpp
HRESULT DoConfigPropsheet(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszTitle,
  LPMAPITABLE lpDisplayTable,
  LPMAPIPROP lpConfigData,
  ULONG ulTopPage
);
```

## <a name="parameters"></a><span data-ttu-id="c9a3d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9a3d-106">Parameters</span></span>

 <span data-ttu-id="c9a3d-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c9a3d-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="c9a3d-108">dans Handle de la fenêtre parent de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="c9a3d-108">[in] A handle to the parent window of the property sheet.</span></span>
    
 <span data-ttu-id="c9a3d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c9a3d-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c9a3d-110">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="c9a3d-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c9a3d-111">_lpszTitle_</span><span class="sxs-lookup"><span data-stu-id="c9a3d-111">_lpszTitle_</span></span>
  
> <span data-ttu-id="c9a3d-112">dans Pointeur vers le titre de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="c9a3d-112">[in] A pointer to the title of the property sheet.</span></span>
    
 <span data-ttu-id="c9a3d-113">_lpDisplayTable_</span><span class="sxs-lookup"><span data-stu-id="c9a3d-113">_lpDisplayTable_</span></span>
  
> <span data-ttu-id="c9a3d-114">dans Pointeur vers la table d'affichage qui décrit les contrôles à afficher sur la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="c9a3d-114">[in] A pointer to the display table that describes the controls to appear on the property sheet.</span></span>
    
 <span data-ttu-id="c9a3d-115">_lpConfigData_</span><span class="sxs-lookup"><span data-stu-id="c9a3d-115">_lpConfigData_</span></span>
  
> <span data-ttu-id="c9a3d-116">dans Pointeur vers l'implémentation [IMAPIProp](imapipropiunknown.md) à utiliser pour accéder aux propriétés de configuration à afficher sur la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="c9a3d-116">[in] A pointer to the [IMAPIProp](imapipropiunknown.md) implementation to be used for accessing the configuration properties to be displayed on the property sheet.</span></span> 
    
 <span data-ttu-id="c9a3d-117">_ulTopPage_</span><span class="sxs-lookup"><span data-stu-id="c9a3d-117">_ulTopPage_</span></span>
  
> <span data-ttu-id="c9a3d-118">dans Index de base zéro de la page supérieure par défaut de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="c9a3d-118">[in] A zero-based index to the default top page of the property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c9a3d-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c9a3d-119">Return value</span></span>

<span data-ttu-id="c9a3d-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9a3d-120">S_OK</span></span> 
  
> <span data-ttu-id="c9a3d-121">La feuille de propriétés de configuration s'est affichée.</span><span class="sxs-lookup"><span data-stu-id="c9a3d-121">The configuration property sheet was displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c9a3d-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="c9a3d-122">Remarks</span></span>

<span data-ttu-id="c9a3d-123">La méthode **IMAPISupport::D oconfigpropsheet** est implémentée pour tous les objets de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c9a3d-123">The **IMAPISupport::DoConfigPropsheet** method is implemented for all support objects.</span></span> <span data-ttu-id="c9a3d-124">**DoConfigPropSheet** fournit une interface utilisateur standard pour afficher les propriétés des fournisseurs de services et des services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c9a3d-124">**DoConfigPropSheet** provides a standard user interface for displaying the properties of service providers and message services.</span></span> <span data-ttu-id="c9a3d-125">Vous devez utiliser cette boîte de dialogue standard pour tous les affichages de propriétés de configuration afin que les utilisateurs bénéficient d'une interface Windows cohérente.</span><span class="sxs-lookup"><span data-stu-id="c9a3d-125">You should use this standard dialog box for all configuration property displays so that users benefit from a consistent Windows interface.</span></span> 
  
<span data-ttu-id="c9a3d-126">Les fournisseurs de services appellent **DoConfigPropSheet** dans le cadre de l'implémentation de la méthode [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) ou à partir d'un bouton utilisé pour afficher des détails sur les propriétés.</span><span class="sxs-lookup"><span data-stu-id="c9a3d-126">Service providers call **DoConfigPropSheet** as part of their implementation of the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method or from a button used to display details on properties.</span></span> <span data-ttu-id="c9a3d-127">Les services de messagerie appellent **DoConfigPropSheet** à partir de la fonction de point d'entrée de service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c9a3d-127">Message services call **DoConfigPropSheet** from their message service entry point function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c9a3d-128">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="c9a3d-128">Notes to callers</span></span>

<span data-ttu-id="c9a3d-129">Vous pouvez créer la table d'affichage désignée par le paramètre _lpDisplayTable_ en appelant la fonction [BuildDisplayTable](builddisplaytable.md) ou avec du code personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c9a3d-129">You can create the display table pointed to by the  _lpDisplayTable_ parameter by calling the [BuildDisplayTable](builddisplaytable.md) function or with custom code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c9a3d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9a3d-130">See also</span></span>



[<span data-ttu-id="c9a3d-131">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="c9a3d-131">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="c9a3d-132">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="c9a3d-132">CreateIProp</span></span>](createiprop.md)
  
[<span data-ttu-id="c9a3d-133">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="c9a3d-133">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="c9a3d-134">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c9a3d-134">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="c9a3d-135">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="c9a3d-135">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="c9a3d-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c9a3d-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="c9a3d-137">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="c9a3d-137">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="c9a3d-138">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="c9a3d-138">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="c9a3d-139">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c9a3d-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

