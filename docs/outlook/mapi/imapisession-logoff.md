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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 317c3702415ddf30038ccd0d40cdf0f19abc61f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338107"
---
# <a name="imapisessionlogoff"></a>IMAPISession::Logoff

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
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
  
> [in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres à afficher. Ce paramètre est ignoré si l’MAPI_LOGOFF_UI n’est pas définie.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôlent l’opération de ffage de logo. Les indicateurs suivants peuvent être définies :
    
MAPI_LOGOFF_SHARED 
  
> Si cette session est partagée, tous les clients qui se sont connectés à l’aide de la session partagée doivent être avertis de la ouverture de session en cours. Les clients doivent se déconnecter. Tout client qui utilise la session partagée peut définir cet indicateur. MAPI_LOGOFF_SHARED est ignoré si la session en cours n’est pas partagée.
    
MAPI_LOGOFF_UI 
  
> **La ff** de logo peut afficher une boîte de dialogue pendant l’opération, éventuellement en insurant à l’utilisateur une confirmation. 
    
 _ulReserved_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’opération de ffage de logo a réussi.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISession::Logoff** met fin à une session MAPI. Lorsque **la méthode Logoff** est de retour, aucune des méthodes à l’exception de [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) ne peut être appelée. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque **la méthode Logoff est** de retour, relâchez l’objet de session en appelant sa méthode **IUnknown::Release.** 
  
Pour plus d’informations sur la fin d’une session, voir [Fin d’une session MAPI.](ending-a-mapi-session.md)
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::Logoff  <br/> |MFCMAPI utilise la méthode **IMAPISession::Logoff** pour se déconnecter de la session avant de la libérer.  <br/> |
   
> [!NOTE]
> En raison du comportement d’arrêt rapide introduit dans Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010 et Microsoft Outlook 2013, les clients ne doivent jamais transmettre le paramètre **MAPI_LOGOFF_SHARED** à [IMAPISession::Logoff](imapisession-logoff.md). Le **MAPI_LOGOFF_SHARED’arrêt** entraîne l’arrêt de tous les clients MAPI et un comportement inattendu se produit. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Fin d’une session MAPI](ending-a-mapi-session.md)

