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
ms.openlocfilehash: 3b3499de9446c83cfc3b97b4d6b02e7c430b65f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586395"
---
# <a name="imapisupportdoconfigpropsheet"></a><span data-ttu-id="8bee8-103">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="8bee8-103">IMAPISupport::DoConfigPropsheet</span></span>

  
  
<span data-ttu-id="8bee8-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bee8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bee8-105">Affiche une feuille de propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="8bee8-105">Displays a configuration property sheet.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="8bee8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8bee8-106">Parameters</span></span>

 <span data-ttu-id="8bee8-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="8bee8-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="8bee8-108">[in] Un handle vers la fenêtre parent de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8bee8-108">[in] A handle to the parent window of the property sheet.</span></span>
    
 <span data-ttu-id="8bee8-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8bee8-109">_ulFlags_</span></span>
  
> <span data-ttu-id="8bee8-110">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="8bee8-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="8bee8-111">_lpszTitle_</span><span class="sxs-lookup"><span data-stu-id="8bee8-111">_lpszTitle_</span></span>
  
> <span data-ttu-id="8bee8-112">[in] Pointeur vers le titre de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8bee8-112">[in] A pointer to the title of the property sheet.</span></span>
    
 <span data-ttu-id="8bee8-113">_lpDisplayTable_</span><span class="sxs-lookup"><span data-stu-id="8bee8-113">_lpDisplayTable_</span></span>
  
> <span data-ttu-id="8bee8-114">[in] Pointeur vers la table d’affichage qui décrit les contrôles qui doit apparaître dans la feuille des propriétés.</span><span class="sxs-lookup"><span data-stu-id="8bee8-114">[in] A pointer to the display table that describes the controls to appear on the property sheet.</span></span>
    
 <span data-ttu-id="8bee8-115">_lpConfigData_</span><span class="sxs-lookup"><span data-stu-id="8bee8-115">_lpConfigData_</span></span>
  
> <span data-ttu-id="8bee8-116">[in] Pointeur vers l’implémentation [IMAPIProp](imapipropiunknown.md) à utiliser pour accéder aux propriétés de configuration pour être affichés sur la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8bee8-116">[in] A pointer to the [IMAPIProp](imapipropiunknown.md) implementation to be used for accessing the configuration properties to be displayed on the property sheet.</span></span> 
    
 <span data-ttu-id="8bee8-117">_ulTopPage_</span><span class="sxs-lookup"><span data-stu-id="8bee8-117">_ulTopPage_</span></span>
  
> <span data-ttu-id="8bee8-118">[in] Index de base zéro à la page principale par défaut de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8bee8-118">[in] A zero-based index to the default top page of the property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8bee8-119">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="8bee8-119">Return value</span></span>

<span data-ttu-id="8bee8-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="8bee8-120">S_OK</span></span> 
  
> <span data-ttu-id="8bee8-121">La feuille de propriétés de configuration a été affichée.</span><span class="sxs-lookup"><span data-stu-id="8bee8-121">The configuration property sheet was displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8bee8-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="8bee8-122">Remarks</span></span>

<span data-ttu-id="8bee8-123">La méthode **IMAPISupport::DoConfigPropsheet** est implémentée pour tous les objets de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8bee8-123">The **IMAPISupport::DoConfigPropsheet** method is implemented for all support objects.</span></span> <span data-ttu-id="8bee8-124">**DoConfigPropSheet** fournit une interface utilisateur standard pour afficher les propriétés de fournisseurs de services et les services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="8bee8-124">**DoConfigPropSheet** provides a standard user interface for displaying the properties of service providers and message services.</span></span> <span data-ttu-id="8bee8-125">Vous devez utiliser cette boîte de dialogue standard pour tous les affichages de propriété de configuration afin que les utilisateurs bénéficient d’une interface cohérente de Windows.</span><span class="sxs-lookup"><span data-stu-id="8bee8-125">You should use this standard dialog box for all configuration property displays so that users benefit from a consistent Windows interface.</span></span> 
  
<span data-ttu-id="8bee8-126">Fournisseurs de services d’appel **DoConfigPropSheet** dans le cadre de leur mise en œuvre de la méthode [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) ou d’un bouton permettant d’afficher plus d’informations sur les propriétés.</span><span class="sxs-lookup"><span data-stu-id="8bee8-126">Service providers call **DoConfigPropSheet** as part of their implementation of the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method or from a button used to display details on properties.</span></span> <span data-ttu-id="8bee8-127">Services de messagerie appellent **DoConfigPropSheet** à partir de leur fonction de point d’entrée de message service.</span><span class="sxs-lookup"><span data-stu-id="8bee8-127">Message services call **DoConfigPropSheet** from their message service entry point function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8bee8-128">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="8bee8-128">Notes to callers</span></span>

<span data-ttu-id="8bee8-129">Vous pouvez créer un affichage désigné par le paramètre _lpDisplayTable_ en appelant la fonction [BuildDisplayTable](builddisplaytable.md) ou avec du code personnalisé.</span><span class="sxs-lookup"><span data-stu-id="8bee8-129">You can create the display table pointed to by the  _lpDisplayTable_ parameter by calling the [BuildDisplayTable](builddisplaytable.md) function or with custom code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8bee8-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bee8-130">See also</span></span>



[<span data-ttu-id="8bee8-131">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="8bee8-131">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="8bee8-132">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="8bee8-132">CreateIProp</span></span>](createiprop.md)
  
[<span data-ttu-id="8bee8-133">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="8bee8-133">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="8bee8-134">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8bee8-134">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="8bee8-135">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="8bee8-135">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="8bee8-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8bee8-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="8bee8-137">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="8bee8-137">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="8bee8-138">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="8bee8-138">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="8bee8-139">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8bee8-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

