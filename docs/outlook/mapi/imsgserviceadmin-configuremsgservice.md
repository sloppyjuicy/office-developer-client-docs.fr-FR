---
title: IMsgServiceAdminConfigureMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.ConfigureMsgService
api_type:
- COM
ms.assetid: a08f5905-2585-49ca-abb7-a77f2736f604
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a599a6fe5093e52e50d33a1761df5689b7335138
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568293"
---
# <a name="imsgserviceadminconfiguremsgservice"></a>IMsgServiceAdmin::ConfigureMsgService

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
RECONFIGURE un service de message.
  
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
  
> [in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique pour le service de message à configurer. 
    
 _ulUIParam_
  
> [in] Un handle vers la fenêtre parent de la feuille de propriétés de configuration.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’affichage de la feuille de propriétés. Les indicateurs suivants peuvent être définis :
    
MAPI_UNICODE 
  
> Les chaînes passée sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
MSG_SERVICE_UI_READ_ONLY 
  
> Le service de message doit afficher sa feuille de propriétés de configuration, mais pas permettre à l’utilisateur à modifier. La plupart des services de messagerie ignorent cet indicateur.
    
SERVICE_UI_ALLOWED 
  
> Le service de message doit afficher sa feuille de propriétés de configuration uniquement si le service n’est pas entièrement configuré.
    
SERVICE_UI_ALWAYS 
  
> Le service de message doit toujours afficher sa feuille de propriétés de configuration. Si SERVICE_UI_ALWAYS n’est pas défini, une feuille de propriétés de configuration peut toujours être affichée si SERVICE_UI_ALLOWED est défini et les informations de configuration valides ne sont pas disponibles dans le tableau de valeurs de propriété dans le paramètre _lpProps_ . SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS doit être définie pour une feuille de propriétés à afficher. 
    
 _cValues_
  
> [in] Le nombre de valeurs de propriété dans la structure [SPropValue](spropvalue.md) désignés par _lpProps_. 
    
 _lpProps_
  
> [in] Pointeur vers un tableau de valeurs de propriété qui décrivent les propriétés à afficher dans la feuille des propriétés. Le paramètre _lpProps_ ne doit pas être NULL si le service de message doit être configuré sans interface utilisateur. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le service de message a été correctement configuré.
    
MAPI_E_EXTENDED_ERROR 
  
> Une erreur spécifique à un service de message. Pour obtenir la structure [MAPIERROR](mapierror.md) qui décrit l’erreur, l’application cliente doit appeler la méthode [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) . 
    
MAPI_E_NOT_FOUND 
  
> Le **MAPIUID** désignés par _lpUID_ ne correspond pas à celui d’un service de message existant. 
    
MAPI_E_NOT_INITIALIZED 
  
> Le service message n’a pas d’entrée de fonction de point.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans la feuille des propriétés. 
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::ConfigureMsgService** permet à un service de message à configurer, avec ou sans une feuille de propriétés de configuration. 
  
Pour permettre la configuration sans un affichage feuille des propriétés, services message préparent généralement un fichier d’en-tête qui contient des constantes pour toutes les propriétés obligatoires et facultatifs et leurs valeurs.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour récupérer la structure **MAPIUID** pour le service de message configurer, récupérer la colonne **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) à partir de la ligne du service de message dans la table de service de message. Pour plus d’informations, voir la procédure décrite dans la méthode [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) . 
  
Vous pouvez configurer un service de message sans afficher une feuille de propriétés à un utilisateur uniquement si vous disposez des informations supplémentaires sur les valeurs de propriété à définir. Si vous configurez un service de message sans afficher une feuille de propriétés, passer des valeurs de propriété valide dans le paramètre _lpProps_ et ne définissez pas les indicateurs MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS. 
  
Si vous recevez tout ou partie des informations de configuration de l’utilisateur par une feuille de propriétés, définissez SERVICE_UI_ALLOWED dans _ulFlags_. Si vous utilisez les informations de propriété existantes uniquement établir des paramètres par défaut et l’utilisateur est en mesure de modifier les paramètres, définissez SERVICE_UI_ALWAYS dans _ulFlags_.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI utilise la méthode **IMsgServiceAdmin::ConfigureMsgService** pour configurer un service qui a été ajouté à un profil.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[SPropValue](spropvalue.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

