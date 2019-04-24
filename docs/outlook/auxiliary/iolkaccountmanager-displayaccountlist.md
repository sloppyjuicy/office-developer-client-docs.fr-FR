---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Affiche la boîte de dialogue Paramètres du compte ou ajouter un nouveau compte.
ms.openlocfilehash: ecf5242fa4f224516e12e667ab66fd0adfe4a25d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322063"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a>IOlkAccountManager::DisplayAccountList

Affiche la boîte de dialogue **paramètres du compte** ou **Ajouter un nouveau compte** . 
  
## <a name="quick-info"></a>Informations rapides

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::DisplayAccountList ( 
    HWND hwnd,
    DWORD dwFlags,
    LPCWSTR wszTitle,
    DWORD cCategories,
    const CLSID * rgclsidCategories,
    const CLSID * pclsidType
);

```

## <a name="parameters"></a>Paramètres

_hwnd_
  
> dans Handle de la fenêtre vers laquelle la boîte de dialogue affichée est modale. Peut être zéro.
    
_dwFlags_
  
> dans Indicateurs permettant de modifier le comportement de l'affichage. 
    
   - **ACCTUI_NO_WARNING**: n'affiche pas l'avertissement signalant que les modifications ne prendront effet qu'après le reDémarrage d'Outlook. S'applique uniquement si l'application est en cours d'exécution dans le processus avec Outlook. exe.
    
   - **ACCTUI_SHOW_DATA_TAB**— affiche la boîte de dialogue **paramètres du compte** avec l'onglet **données** sélectionné. Valide uniquement si **ACCTUI_SHOW_ACCTWIZARD** n'est pas défini. 
    
   - **ACCTUI_SHOW_ACCTWIZARD**: affiche la boîte de dialogue **Ajouter un nouveau compte** . 
    
_wszTitle_
  
> dans Ce paramètre n'est pas utilisé et doit être NULL.
    
_cCategories_
  
> dans Ce paramètre n'est pas utilisé et doit être NULL. 
    
_rgclsidCategories_
  
> dans Ce paramètre n'est pas utilisé et doit être NULL.
    
_pclsidType_
  
> dans Ce paramètre n'est pas utilisé et doit être NULL.
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi.  <br/> |
|E_ACCT_UI_BUSY  <br/> |La boîte de dialogue n'a pas pu être créée.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |La boîte de dialogue **Ajouter un nouveau compte** a renvoyé une erreur.  <br/> |
|MAPI_E_INVALID_PARAMETER  <br/> |Le paramètre _cCategories_, _rgclsidCategories_ou _pclsidType_ est non null.  <br/> |
|MAPI_E_USER_CANCEL  <br/> |La boîte de dialogue **paramètres du compte** a renvoyé une erreur.  <br/> |
   
## <a name="remarks"></a>Remarques

Les paramètres _cCategories_, _rgclsidCategories_et _pclsidType_ ne sont pas utilisés pour le moment et doivent être null.  _wszTitle_ n'est pas utilisé et doit également avoir la valeur null. 
  

