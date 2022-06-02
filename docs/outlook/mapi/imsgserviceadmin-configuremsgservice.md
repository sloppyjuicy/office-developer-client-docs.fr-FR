---
title: IMsgServiceAdminConfigureMsgService
description: Décrit la syntaxe, les paramètres, la valeur de retour et les remarques pour IMsgServiceAdminConfigureMsgService, qui reconfigure un service de message.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.ConfigureMsgService
api_type:
- COM
ms.assetid: a08f5905-2585-49ca-abb7-a77f2736f604
ms.openlocfilehash: a3caef017f0d045429a35ab5cba6b7e60b20503b
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828573"
---
# <a name="imsgserviceadminconfiguremsgservice"></a>IMsgServiceAdmin::ConfigureMsgService

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Reconfigure un service de message.
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a>Paramètres

 _lpUID_
  
> [in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique du service de message à configurer. 
    
 _ulUIParam_
  
> [in] Handle de la fenêtre parente de la feuille de propriétés de configuration.
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle l’affichage de la feuille de propriétés. Les indicateurs suivants peuvent être définis :
    
MAPI_UNICODE 
  
> Les chaînes passées sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, les chaînes sont au format ANSI.
    
MSG_SERVICE_UI_READ_ONLY 
  
> Le service de message doit afficher sa feuille de propriétés de configuration, mais pas permettre à l’utilisateur de la modifier. La plupart des services de messages ignorent cet indicateur.
    
SERVICE_UI_ALLOWED 
  
> Le service de message doit afficher sa feuille de propriétés de configuration uniquement si le service n’est pas entièrement configuré.
    
SERVICE_UI_ALWAYS 
  
> Le service de message doit toujours afficher sa feuille de propriétés de configuration. Si SERVICE_UI_ALWAYS n’est pas défini, une feuille de propriétés de configuration peut toujours être affichée si SERVICE_UI_ALLOWED est défini et si les informations de configuration valides ne sont pas disponibles à partir du tableau de valeurs de propriétés dans le paramètre _lpProps_ . Vous devez définir SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS pour qu’une feuille de propriétés s’affiche. 
    
 _cValues_
  
> [in] Nombre de valeurs de propriété dans la structure [SPropValue](spropvalue.md) pointée par  _lpProps_. 
    
 _lpProps_
  
> [in] Pointeur vers un tableau de valeurs de propriétés qui décrivent les propriétés à afficher dans la feuille de propriétés. Le paramètre  _lpProps_ ne doit pas être NULL si le service de message doit être configuré sans interface utilisateur. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le service de message a été correctement configuré.
    
MAPI_E_EXTENDED_ERROR 
  
> Erreur spécifique à un service de message. Pour obtenir la structure [MAPIERROR](mapierror.md) qui décrit l’erreur, l’application cliente doit appeler la méthode [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) . 
    
MAPI_E_NOT_FOUND 
  
> Le **MAPIUID** pointé par  _lpUID_ ne correspond pas à celui d’un service de message existant. 
    
MAPI_E_NOT_INITIALIZED 
  
> Le service de message n’a pas de fonction de point d’entrée.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération, généralement en cliquant sur le bouton **Annuler** dans la feuille de propriétés. 
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::ConfigureMsgService** permet de configurer un service de message, avec ou sans feuille de propriétés de configuration. 
  
Pour autoriser la configuration sans affichage de feuille de propriétés, les services de messages préparent généralement un fichier d’en-tête qui inclut des constantes pour toutes les propriétés requises et facultatives et leurs valeurs.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour récupérer la structure **MAPIUID** du service de message à configurer, récupérez la colonne **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) à partir de la ligne du service de message dans la table du service de messages. Pour plus d’informations, consultez la procédure décrite dans la méthode [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) . 
  
Vous pouvez configurer un service de message sans afficher de feuille de propriétés à un utilisateur uniquement si vous disposez d’informations préalables sur les valeurs de propriété à définir. Si vous configurez un service de message sans afficher de feuille de propriétés, transmettez des valeurs de propriété valides dans le paramètre _lpProps_ et ne définissez pas les indicateurs MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS. 
  
Si vous recevez l’ensemble ou une partie des informations de configuration de l’utilisateur par le moyen d’une feuille de propriétés, définissez SERVICE_UI_ALLOWED dans  _ulFlags_. Si vous utilisez des informations de propriété existantes uniquement pour établir des paramètres par défaut et que l’utilisateur est en mesure de modifier les paramètres, définissez SERVICE_UI_ALWAYS dans  _ulFlags_.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI utilise la méthode **IMsgServiceAdmin::ConfigureMsgService** pour configurer un service qui a été ajouté à un profil. |
   
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[SPropValue](spropvalue.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

