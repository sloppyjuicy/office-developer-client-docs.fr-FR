---
title: IMsgServiceAdminCreateMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CreateMsgService
api_type:
- COM
ms.assetid: 0135f049-0311-45e5-9685-78597d599a4e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e7d30c1aba8ddc1419045c1caa8524f7d2063dc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434976"
---
# <a name="imsgserviceadmincreatemsgservice"></a>IMsgServiceAdmin::CreateMsgService

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Déconseillé: l'utilisation de [IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) est recommandée. Ajoute un service de messagerie au profil actif. 
  
```cpp
HRESULT CreateMsgService(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>Paramètres

 _lpszService_
  
> dans Pointeur vers le nom du service de messagerie à ajouter. Ce nom de service de message doit apparaître dans la section **[services]** du fichier MapiSvc. inf. 
    
 _lpszDisplayName_
  
> dans Pointeur vers le nom d'affichage du service de messagerie à ajouter. Le paramètre _lpszDisplayName_ est ignoré si le service de messagerie a défini la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) dans le fichier MapiSvc. inf.
    
 _ulUIParam_
  
> dans Handle de la fenêtre parente de toutes les boîtes de dialogue ou fenêtres que cette méthode affiche.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'installation du service de messagerie. Les indicateurs suivants peuvent être définis:
    
MAPI_UNICODE
  
> Les paramètres lpszService et lpszDisplayName doivent être castés en LPWSTR et interprétés comme des chaînes Unicode.
    
SERVICE_NO_RESTART_WARNING
  
> Lors de l'ajout d'un nouveau service de messagerie au profil, le sous-système MAPI, basé sur différentes circonstances et critères, détermine souvent que cette action nécessite un redémarrage d'Outlook. Si l'indicateur SERVICE_NO_RESTART_WARNING n'est pas inclus et que l'interface utilisateur est autorisée (en fonction des indicateurs SERVICE_UI_ALWAYS et SERVICE_UI_ALLOWED) et qu'au moins un processus est connecté au profil actuel, cette fonction affiche le message «vous devez redémarrer Outlook pour Ces modifications prennent effet. " L'ajout de l'indicateur SERVICE_NO_RESTART_WARNING supprime l'affichage de ce message d'avertissement.
    
SERVICE_UI_ALLOWED
  
> L'interface utilisateur de configuration du service de messagerie est autorisée si nécessaire.
    
SERVICE_UI_ALWAYS 
  
> Le service de messagerie affiche sa feuille de propriétés de configuration.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NOT_FOUND 
  
> Le nom du service de messagerie ne figure pas dans la section **[services]** du fichier MapiSvc. inf. 
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin:: CreateMsgService** ajoute un service de messagerie au profil actif. **CreateMsgService** appelle la fonction de point d'entrée du service de messagerie pour effectuer les tâches de configuration propres au service. Si l'indicateur SERVICE_UI_ALLOWED est défini dans le paramètre _ulFlags_ , le service de messagerie en cours d'installation peut afficher une feuille de propriétés pour permettre à l'utilisateur de configurer ses paramètres. 
  
Le fichier MapiSvc. INF contient la liste des fournisseurs qui composent un service de messagerie et les propriétés de chacune d'elles. **CreateMsgService** crée d'abord une section de profil pour le service de messagerie, puis copie toutes les informations pour ce service à partir du fichier MapiSvc. inf dans le profil, créant de nouvelles sections pour chaque fournisseur. 
  
Une fois que toutes les informations ont été copiées à partir de MapiSvc. inf, la fonction de point d'entrée du service de messagerie est appelée avec la valeur MSG_SERVICE_CREATE définie dans le paramètre _ulContext_ . Si l'indicateur SERVICE_UI_ALLOWED est défini dans le paramètre _ulFlags_ de la méthode **CreateMsgService** , les valeurs des paramètres _ulUIParam_ et _ulFlags_ sont également transmises lors de l'appel à la fonction point d'entrée du service de messagerie. Les fournisseurs de services doivent afficher leurs feuilles de propriétés de configuration afin que les utilisateurs puissent configurer le service de messagerie. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

 **CreateMsgService** ne retourne pas la structure [MAPIUID](mapiuid.md) pour le service de messagerie qui a été ajouté au profil. 
  
Pour récupérer le **MAPIUID** pour le service de messagerie créé, procédez comme suit: 
  
1. Appelez la méthode [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) pour obtenir la table d'administration des services de messagerie. 
    
2. Localisez la ligne qui représente le service de messagerie en plaçant une restriction sur la table qui correspond à la propriété **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) avec le nom du service de messagerie. 
    
3. Récupérez la propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) du service. 
    
4. TransMettez la valeur de la propriété **PR_SERVICE_UID** dans le paramètre _lpUid_ à la méthode [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) pour configurer le service. 
    
> [!CAUTION]
> L'implémentation Microsoft Outlook 2010 du sous-système MAPI ne prend pas en charge MAPI_UNICODE et échoue si elle est utilisée. 
  
> [!IMPORTANT]
> Le _ulFlags_ SERVICE_NO_RESTART_WARNING peut ne pas être défini dans le fichier d'en-tête téléchargeable dont vous disposez actuellement, auquel cas vous pouvez l'ajouter à votre code à l'aide de la valeur suivante: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions. cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI utilise la méthode **IMsgServiceAdmin:: CreateMsgService** pour ajouter un service à un profil.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

