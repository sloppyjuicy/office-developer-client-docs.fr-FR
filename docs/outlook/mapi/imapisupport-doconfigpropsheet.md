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
# <a name="imapisupportdoconfigpropsheet"></a>IMAPISupport::DoConfigPropsheet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Affiche une feuille de propriétés de configuration.
  
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

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Poignée vers la fenêtre parente de la feuille des propriétés.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpszTitle_
  
> [in] Pointeur vers le titre de la feuille des propriétés.
    
 _lpDisplayTable_
  
> [in] Pointeur vers le tableau d’affichage qui décrit les contrôles à afficher dans la feuille des propriétés.
    
 _lpConfigData_
  
> [in] Pointeur vers [l’implémentation IMAPIProp](imapipropiunknown.md) à utiliser pour accéder aux propriétés de configuration à afficher dans la feuille des propriétés. 
    
 _ulTopPage_
  
> [in] Index de base zéro vers la page supérieure par défaut de la feuille des propriétés.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La feuille des propriétés de configuration a été affichée.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::D oConfigPropsheet** est implémentée pour tous les objets de prise en charge. **DoConfigPropSheet** fournit une interface utilisateur standard pour l’affichage des propriétés des fournisseurs de services et des services de messagerie. Vous devez utiliser cette boîte de dialogue standard pour tous les affichages de propriété de configuration afin que les utilisateurs bénéficient d’une interface Windows cohérente. 
  
Les fournisseurs de services **appellent DoConfigPropSheet** dans le cadre de leur implémentation de la méthode [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) ou à partir d’un bouton utilisé pour afficher des détails sur les propriétés. Les services de messages **appellent DoConfigPropSheet à** partir de leur fonction de point d’entrée de service de message. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez créer le tableau d’affichage pointé par le paramètre  _lpDisplayTable_ en appelant la [fonction BuildDisplayTable](builddisplaytable.md) ou avec du code personnalisé. 
  
## <a name="see-also"></a>Voir aussi



[BuildDisplayTable](builddisplaytable.md)
  
[CreateIProp](createiprop.md)
  
[IABProvider::Logon](iabprovider-logon.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

