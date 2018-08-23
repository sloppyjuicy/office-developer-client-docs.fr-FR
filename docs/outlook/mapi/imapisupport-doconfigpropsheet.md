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
# <a name="imapisupportdoconfigpropsheet"></a>IMAPISupport::DoConfigPropsheet

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Un handle vers la fenêtre parent de la feuille de propriétés.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpszTitle_
  
> [in] Pointeur vers le titre de la feuille de propriétés.
    
 _lpDisplayTable_
  
> [in] Pointeur vers la table d’affichage qui décrit les contrôles qui doit apparaître dans la feuille des propriétés.
    
 _lpConfigData_
  
> [in] Pointeur vers l’implémentation [IMAPIProp](imapipropiunknown.md) à utiliser pour accéder aux propriétés de configuration pour être affichés sur la feuille de propriétés. 
    
 _ulTopPage_
  
> [in] Index de base zéro à la page principale par défaut de la feuille de propriétés.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La feuille de propriétés de configuration a été affichée.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::DoConfigPropsheet** est implémentée pour tous les objets de prise en charge. **DoConfigPropSheet** fournit une interface utilisateur standard pour afficher les propriétés de fournisseurs de services et les services de messagerie. Vous devez utiliser cette boîte de dialogue standard pour tous les affichages de propriété de configuration afin que les utilisateurs bénéficient d’une interface cohérente de Windows. 
  
Fournisseurs de services d’appel **DoConfigPropSheet** dans le cadre de leur mise en œuvre de la méthode [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) ou d’un bouton permettant d’afficher plus d’informations sur les propriétés. Services de messagerie appellent **DoConfigPropSheet** à partir de leur fonction de point d’entrée de message service. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez créer un affichage désigné par le paramètre _lpDisplayTable_ en appelant la fonction [BuildDisplayTable](builddisplaytable.md) ou avec du code personnalisé. 
  
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

