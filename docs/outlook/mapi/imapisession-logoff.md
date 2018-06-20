---
title: IMAPISessionLogoff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Logoff
api_type:
- COM
ms.assetid: 93e38f6c-4b67-4f2d-bc94-631efec86852
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7d6ccd64fea0af30e81a2db0bcb9630062b4b64d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783928"
---
# <a name="imapisessionlogoff"></a>IMAPISession::Logoff

  
  
**S’applique à**: Outlook 
  
Met fin à une session MAPI.
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Handle vers la fenêtre parent de toutes les boîtes de dialogue ou fenêtre à afficher. Ce paramètre est ignoré si l’indicateur MAPI_LOGOFF_UI n’est pas définie.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôlent l’opération de déconnexion. Les indicateurs suivants peuvent être définis :
    
MAPI_LOGOFF_SHARED 
  
> Si cette session est partagée, tous les clients qui a ouvert une session à l’aide de la session partagée doivent être informés de la fermeture de session en cours. Les clients doivent se déconnectent. Tout client qui est à l’aide de la session partagée peut définir cet indicateur. MAPI_LOGOFF_SHARED est ignorée si la session en cours n’est pas partagée.
    
MAPI_LOGOFF_UI 
  
> **Fermeture de session** peut afficher une boîte de dialogue lors de l’opération, éventuellement inviter l’utilisateur à confirmer. 
    
 _ulReserved_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’opération de fermeture de session a réussi.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::Logoff** termine une session MAPI. Lors de la **fermeture de session** renvoie, aucune des méthodes à l’exception de [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) peut être appelée. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Lors de la **fermeture de session** renvoie, version de l’objet de la session en appelant la méthode **IUnknown::Release** . 
  
Pour plus d’informations sur la fin d’une session, voir [mettre fin à une Session MAPI](ending-a-mapi-session.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::Logoff  <br/> |MFCMAPI utilise la méthode **IMAPISession::Logoff** pour déconnecter la session avant de les mettre.  <br/> |
   
> [!NOTE]
> En raison du comportement d’arrêt rapide introduit dans Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010 et Microsoft Outlook 2013, les clients doivent jamais passer le paramètre **MAPI_LOGOFF_SHARED** à [IMAPISession::Logoff](imapisession-logoff.md). Passage **MAPI_LOGOFF_SHARED** provoque tous les clients MAPI commencer l’arrêt et un comportement inattendu se produit. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Mettre fin à une Session MAPI](ending-a-mapi-session.md)

