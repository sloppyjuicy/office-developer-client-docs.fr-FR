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
ms.openlocfilehash: 87ac394f9ab77b092cdfcd44f65b040a039319e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422186"
---
# <a name="imsgserviceadminconfiguremsgservice"></a>IMsgServiceAdmin::ConfigureMsgService

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Reconfigure un service de messagerie.
  
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
  
> dans Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l'identificateur unique pour le service de messagerie à configurer. 
    
 _ulUIParam_
  
> dans Handle de la fenêtre parente de la feuille de propriétés de configuration.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle l'affichage de la feuille de propriétés. Les indicateurs suivants peuvent être définis:
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.
    
MSG_SERVICE_UI_READ_ONLY 
  
> Le service de messagerie doit afficher sa feuille de propriétés de configuration mais ne pas permettre à l'utilisateur de le modifier. La plupart des services de messagerie ignorent cet indicateur.
    
SERVICE_UI_ALLOWED 
  
> Le service de messagerie doit afficher sa feuille de propriétés de configuration uniquement si le service n'est pas entièrement configuré.
    
SERVICE_UI_ALWAYS 
  
> Le service de messagerie doit toujours afficher sa feuille de propriétés de configuration. Si SERVICE_UI_ALWAYS n'est pas défini, une feuille de propriétés de configuration peut toujours être affichée si SERVICE_UI_ALLOWED est défini et que des informations de configuration valides ne sont pas disponibles à partir du tableau de valeurs de propriété dans le paramètre _lpProps_ . SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS doit être défini pour qu'une feuille de propriétés s'affiche. 
    
 _cValues_
  
> dans Nombre de valeurs de propriété dans la structure [SPropValue](spropvalue.md) vers laquelle pointe le _lpProps_. 
    
 _lpProps_
  
> dans Pointeur vers un tableau de valeurs de propriété qui décrivent les propriétés à afficher dans la feuille des propriétés. Le paramètre _lpProps_ ne doit pas être null si le service de messagerie doit être configuré sans interface utilisateur. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le service de messagerie a été correctement configuré.
    
MAPI_E_EXTENDED_ERROR 
  
> Erreur spécifique à un service de messagerie. Pour obtenir la structure [MAPIERROR](mapierror.md) qui décrit l'erreur, l'application cliente doit appeler la méthode [IMsgServiceAdmin:: GetLastError](imsgserviceadmin-getlasterror.md) . 
    
MAPI_E_NOT_FOUND 
  
> Le **MAPIUID** pointé par _lpUID_ ne correspond pas à celui d'un service de messagerie existant. 
    
MAPI_E_NOT_INITIALIZED 
  
> Le service de messagerie n'a pas de fonction de point d'entrée.
    
MAPI_E_USER_CANCEL 
  
> L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton **Annuler** dans la feuille des propriétés. 
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin:: ConfigureMsgService** permet de configurer un service de messagerie, avec ou sans feuille de propriétés de configuration. 
  
Pour autoriser la configuration sans affichage de feuille de propriétés, les services de messagerie préparent généralement un fichier d'en-tête qui inclut des constantes pour toutes les propriétés obligatoires et facultatives, ainsi que leurs valeurs.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour récupérer la structure **MAPIUID** du service de messagerie à configurer, récupérez la colonne **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) à partir de la ligne du service de messagerie dans la table de service de messagerie. Pour plus d'informations, reportez-vous à la procédure décrite dans la méthode [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) . 
  
Vous pouvez configurer un service de messagerie sans afficher de feuille de propriétés à un utilisateur uniquement si vous avez avancé des informations sur les valeurs de propriété à définir. Si vous configurez un service de messagerie sans afficher de feuille de propriétés, transmettez les valeurs de propriété valides dans le paramètre _lpProps_ et ne définissez pas les indicateurs MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS. 
  
Si vous recevez tout ou partie des informations de configuration de l'utilisateur par le biais d'une feuille de propriétés, définissez SERVICE_UI_ALLOWED dans _ulFlags_. Si vous utilisez des informations de propriété existantes uniquement pour établir les paramètres par défaut et que l'utilisateur est en mesure de modifier les paramètres, définissez SERVICE_UI_ALWAYS dans _ulFlags_.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions. cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI utilise la méthode **IMsgServiceAdmin:: ConfigureMsgService** pour configurer un service qui a été ajouté à un profil.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[SPropValue](spropvalue.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

