---
title: IMAPISessionLogoff
description: Décrit la syntaxe, les paramètres, la valeur de retour et les remarques pour IMAPISessionLogoff, qui termine une session MAPI.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.Logoff
api_type:
- COM
ms.assetid: 93e38f6c-4b67-4f2d-bc94-631efec86852
ms.openlocfilehash: bf777c211b0761e90bd0b692276e10ac1d80a65f
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827967"
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
  
> [in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres à afficher. Ce paramètre est ignoré si l’indicateur de MAPI_LOGOFF_UI n’est pas défini.
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôlent l’opération de fermeture de session. Les indicateurs suivants peuvent être définis :
    
MAPI_LOGOFF_SHARED 
  
> Si cette session est partagée, tous les clients qui se sont connectés à l’aide de la session partagée doivent être avertis de la fermeture de session en cours. Les clients doivent se déconnecter. Tout client qui utilise la session partagée peut définir cet indicateur. MAPI_LOGOFF_SHARED est ignoré si la session active n’est pas partagée.
    
MAPI_LOGOFF_UI 
  
> **La fermeture de session** peut afficher une boîte de dialogue pendant l’opération, ce qui peut demander confirmation à l’utilisateur. 
    
 _ulReserved_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’opération de fermeture de session a réussi.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::Logoff** met fin à une session MAPI. Lorsque **Logoff** retourne, aucune des méthodes, à l’exception de [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) , ne peut être appelée. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque **Logoff** retourne, relâchez l’objet de session en appelant sa méthode **IUnknown::Release** . 
  
Pour plus d’informations sur la fin d’une session, consultez [Fin d’une session MAPI](ending-a-mapi-session.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::Logoff  <br/> |MFCMAPI utilise la méthode **IMAPISession::Logoff** pour se déconnecter de la session avant de la libérer. |
   
> [!NOTE]
> En raison du comportement d’arrêt rapide introduit dans Microsoft Office Outlook Service Pack 2, Microsoft Outlook 2010 et Microsoft Outlook 2013 2007, les clients ne doivent jamais passer le paramètre **MAPI_LOGOFF_SHARED** à [IMAPISession::Logoff](imapisession-logoff.md). Le passage **de MAPI_LOGOFF_SHARED** entraîne l’arrêt de tous les clients MAPI et un comportement inattendu se produit. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Fin d’une session MAPI](ending-a-mapi-session.md)

