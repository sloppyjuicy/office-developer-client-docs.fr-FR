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
ms.openlocfilehash: 7c649680d1d04e210ac4d90779e9a4e57aaab25a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579864"
---
# <a name="imsgserviceadmincreatemsgservice"></a>IMsgServiceAdmin::CreateMsgService

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Déconseillée : L’utilisation de [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) est recommandée. Ajoute un service de message pour le profil actuel. 
  
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
  
> [in] Pointeur vers le nom du service de message à ajouter. Ce nom de service de message doit apparaître dans la section **[Services]** du fichier MapiSvc.inf. 
    
 _lpszDisplayName_
  
> [in] Pointeur vers le nom complet du service de message à ajouter. Le paramètre _lpszDisplayName_ est ignoré si le service de message a défini la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) dans le fichier MapiSvc.inf.
    
 _ulUIParam_
  
> [in] Un handle vers la fenêtre parent des boîtes de dialogue ni windows cette méthode affiche.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le service de message est installé. Les indicateurs suivants peuvent être définis :
    
MAPI_UNICODE
  
> Paramètres lpszDisplayName et le lpszService doivent être castés en LPWSTR et interprétées en tant que chaînes Unicode.
    
SERVICE_NO_RESTART_WARNING
  
> Lorsque vous ajoutez un nouveau service de message pour le profil, le sous-système MAPI, selon les circonstances et de différents critères, détermine souvent que cette action nécessite un redémarrage d’Outlook. Si l’indicateur SERVICE_NO_RESTART_WARNING n’est pas inclus, l’interface utilisateur est autorisé - basée sur les indicateurs SERVICE_UI_ALWAYS et SERVICE_UI_ALLOWED - et au moins un processus est connecté le profil actif, cette fonction affiche le message « vous devez redémarrer Outlook pour ces modifications prennent effet. » Y compris l’indicateur SERVICE_NO_RESTART_WARNING supprime l’affichage de ce message d’avertissement.
    
SERVICE_UI_ALLOWED
  
> La configuration du service message si nécessaire, l’interface utilisateur est autorisé.
    
SERVICE_UI_ALWAYS 
  
> Le service de message affiche sa feuille de propriétés de configuration.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NOT_FOUND 
  
> Le nom de service de message n’est pas dans la section **[Services]** du fichier MapiSvc.inf. 
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::CreateMsgService** ajoute un service de message pour le profil actuel. **CreateMsgService** appelle la fonction du point d’entrée du service de message pour effectuer des tâches de configuration spécifiques au service. Si l’indicateur SERVICE_UI_ALLOWED est défini dans le paramètre _ulFlags_ , le service de message en cours d’installation peut afficher une feuille de propriétés pour permettre à l’utilisateur configurer ses paramètres. 
  
Le fichier MapiSvc.inf contient la liste des fournisseurs qui constituent un service de message et les propriétés de chacun. **CreateMsgService** crée d’abord une nouvelle section de profil pour le service de message, puis copie toutes les informations de ce service à partir du fichier MapiSvc.inf dans le profil de la création de nouvelles sections pour chaque fournisseur. 
  
Une fois que toutes les informations a été copiées à partir du fichier MapiSvc.inf, fonction de point d’entrée du service de message est appelée avec la valeur MSG_SERVICE_CREATE définie dans le paramètre _ulContext_ . Si l’indicateur SERVICE_UI_ALLOWED est défini dans le paramètre de la méthode **CreateMsgService** _ulFlags_ , les valeurs dans les paramètres _ulUIParam_ et _ulFlags_ sont également passés à la fonction de point d’entrée du service de message est appelée. Fournisseurs de services doivent afficher leurs feuilles de propriétés de configuration afin que les utilisateurs peuvent configurer le service de message. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

 **CreateMsgService** ne renvoie pas la structure [MAPIUID](mapiuid.md) pour le service de message qui a été ajouté au profil. 
  
Pour récupérer la **MAPIUID** pour le service de message, utilisez la procédure suivante : 
  
1. Appelez la méthode [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) pour obtenir la table de l’administration des services de message. 
    
2. Recherchez la ligne qui représente le service de message en plaçant une restriction sur le tableau qui correspond à la propriété **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) avec le nom du service de message. 
    
3. Récupérer la propriété du service **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)). 
    
4. Passez la valeur de la propriété **PR_SERVICE_UID** dans le paramètre _lpUid_ à la méthode [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) pour configurer le service. 
    
> [!CAUTION]
> L’implémentation Microsoft Outlook 2010 du sous-système MAPI ne prend pas en charge MAPI_UNICODE et échoue si elle est utilisée. 
  
> [!IMPORTANT]
> _ulFlags_ SERVICE_NO_RESTART_WARNING pas peuvent être définis dans le fichier d’en-tête téléchargeables que vous avez actuellement, auquel cas vous pouvez l’ajouter à votre code à l’aide de la valeur suivante : >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI utilise la méthode **IMsgServiceAdmin::CreateMsgService** pour ajouter un service à un profil.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

