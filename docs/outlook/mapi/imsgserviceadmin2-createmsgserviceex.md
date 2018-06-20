---
title: IMsgServiceAdmin2CreateMsgServiceEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin2.CreateMsgServiceEx
api_type:
- COM
ms.assetid: 4910dabd-9380-4fde-a440-5c64d74c0bba
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 3aae61f7b21c507da7955dbb4393d13bfb5fa24c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784227"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a>IMsgServiceAdmin2::CreateMsgServiceEx

  
  
**S’applique à**: Outlook 
  
Ajoute un service de message pour le profil actuel et des retours nouvellement ajouté UID de service.
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
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
    
 _lpuidService_
  
> [out] Pointeur vers l’UID du service de message ajouté.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NOT_FOUND
  
> Le nom de service de message n’est pas dans la section **[Services]** du fichier MapiSvc.inf. 
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin2::CreateMsgServiceEx** ajoute un service de message pour le profil actuel. **CreateMsgServiceEx** appelle la fonction du point d’entrée du service de message pour effectuer des tâches de configuration spécifiques au service. Si l’indicateur SERVICE_UI_ALLOWED est défini dans le paramètre _ulFlags_ , le service de message en cours d’installation peut afficher une feuille de propriétés de l’activation de l’utilisateur de configurer ses paramètres. 
  
Le fichier MapiSvc.inf contient la liste des fournisseurs qui constituent un service de message et les propriétés de chacun. **CreateMsgServiceEx** crée d’abord une nouvelle section de profil pour le service de message, puis copie toutes les informations de ce service à partir du fichier MapiSvc.inf dans le profil de la création de nouvelles sections pour chaque fournisseur. 
  
Une fois que toutes les informations a été copiées à partir du fichier MapiSvc.inf, fonction de point d’entrée du message service **MSGSERVICEENTRY**, est appelée avec la valeur MSG_SERVICE_CREATE définie dans le paramètre _ulContext_ . Si l’indicateur SERVICE_UI_ALLOWED est défini dans le paramètre de la méthode **CreateMsgServiceEx** _ulFlags_ , les valeurs dans les paramètres _ulUIParam_ et _ulFlags_ sont également passés à la fonction de point d’entrée du service de message est appelée. Fournisseurs de services doivent afficher leurs feuilles de propriétés de configuration afin que les utilisateurs peuvent configurer le service de message. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Si l’argument _lpuidService_ **CreateMsgServiceEx** n’est pas NULL, la propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) du service de message qui a été ajouté au profil est renvoyée dans le **GUID** vers laquelle il pointe. 
  
Passez la valeur de la propriété **PR_SERVICE_UID** dans le paramètre _lpuidService_ à la méthode [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) pour configurer le service. 
  
> [!CAUTION]
> L’implémentation Microsoft Outlook 2010 du sous-système MAPI ne prend pas en charge MAPI_UNICODE et échoue si elle est utilisée. 
  
> [!IMPORTANT]
> L’interface IMsgServiceAdmin2 est exposé par le même objet qui implémente l’interface IMsgServiceAdmin et est disponible à l’aide de la mise en œuvre d’Outlook du sous-système MAPI depuis Outlook 2003. Son IID est définie comme suit : > `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> _ulFlags_ SERVICE_NO_RESTART_WARNING pas peuvent être définis dans le fichier d’en-tête téléchargeables que vous avez actuellement, auquel cas vous pouvez l’ajouter à votre code à l’aide de la valeur suivante : >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin2 : IMsgServiceAdmin](imsgserviceadmin2imsgserviceadmin.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

