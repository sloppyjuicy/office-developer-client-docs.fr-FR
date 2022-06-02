---
title: IMsgServiceAdminCreateMsgService
description: IMsgServiceAdmin CreateMsgService est déconseillé et l’utilisation d’IMsgServiceAdmin2 CreateMsgServiceEx est recommandée.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.CreateMsgService
api_type:
- COM
ms.assetid: 0135f049-0311-45e5-9685-78597d599a4e
ms.openlocfilehash: c340d71f4c907894e1ccbf990b9020fe09b5db61
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828373"
---
# <a name="imsgserviceadmincreatemsgservice"></a>IMsgServiceAdmin::CreateMsgService

**S’applique à** : Outlook 2013 | Outlook 2016
  
Déconseillé : L’utilisation [d’IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) est recommandée. Ajoute un service de message au profil actuel.
  
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
  
> [in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le service de message est installé. Les indicateurs suivants peuvent être définis :

MAPI_UNICODE
  
> Les paramètres lpszService et lpszDisplayName doivent être convertis en LPWSTR et interprétés comme des chaînes Unicode.

SERVICE_NO_RESTART_WARNING
  
> Lors de l’ajout d’un nouveau service de message au profil, le sous-système MAPI, en fonction de diverses circonstances et critères, détermine souvent que cette action nécessite un redémarrage de Outlook. Si l’indicateur SERVICE_NO_RESTART_WARNING n’est pas inclus et que l’interface utilisateur est autorisée ( en fonction des indicateurs SERVICE_UI_ALWAYS et SERVICE_UI_ALLOWED ) et qu’au moins un processus est connecté au profil actuel, cette fonction affiche le message « Vous devez redémarrer Outlook pour que ces modifications prennent effet ». L’inclusion de l’indicateur SERVICE_NO_RESTART_WARNING supprime l’affichage de ce message d’avertissement.

SERVICE_UI_ALLOWED
  
> L’interface utilisateur de configuration du service de message est autorisée si nécessaire.

SERVICE_UI_ALWAYS
  
> Le service de message affiche sa feuille de propriétés de configuration.

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.

MAPI_E_NOT_FOUND
  
> Le nom du service de message ne figure pas dans la section **[Services]** de MapiSvc.inf.

## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::CreateMsgService** ajoute un service de message au profil actuel. **CreateMsgService** appelle la fonction de point d’entrée du service de message pour effectuer des tâches de configuration spécifiques au service. Si l’indicateur SERVICE_UI_ALLOWED est défini dans le paramètre _ulFlags_ , le service de message en cours d’installation peut afficher une feuille de propriétés pour permettre à l’utilisateur de configurer ses paramètres.
  
Le fichier MapiSvc.inf contient la liste des fournisseurs qui composent un service de message et les propriétés de chacun d’eux. **CreateMsgService** crée d’abord une section de profil pour le service de message, puis copie toutes les informations de ce service à partir du fichier MapiSvc.inf dans le profil, en créant de nouvelles sections pour chaque fournisseur.
  
Une fois que toutes les informations ont été copiées à partir de MapiSvc.inf, la fonction de point d’entrée du service de message est appelée avec la valeur MSG_SERVICE_CREATE définie dans le paramètre _ulContext_ . Si l’indicateur SERVICE_UI_ALLOWED est défini dans le paramètre _ulFlags_ de la méthode **CreateMsgService**, les valeurs des paramètres _ulUIParam_ et _ulFlags sont également transmises_ lorsque la fonction de point d’entrée du service de message est appelée. Les fournisseurs de services doivent afficher leurs feuilles de propriétés de configuration afin que les utilisateurs puissent configurer le service de message.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

 **CreateMsgService** ne retourne pas la structure [MAPIUID](mapiuid.md) pour le service de message qui a été ajouté au profil.
  
Pour récupérer le **MAPIUID** du service de message créé, procédez comme suit :
  
1. Appelez la méthode [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) pour obtenir la table d’administration du service de message.

2. Recherchez la ligne qui représente le service de message en plaçant une restriction sur la table qui correspond à la propriété **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) avec le nom du service de message.

3. Récupérez la propriété **PR_SERVICE_UID** du service ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)).

4. Transmettez la valeur de la propriété **PR_SERVICE_UID** dans le paramètre _lpUid_ à la méthode [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) pour configurer le service.

> [!CAUTION]
> L’implémentation Microsoft Outlook 2010 du sous-système MAPI ne prend pas en charge MAPI_UNICODE et échoue si elle est utilisée.
  
> [!IMPORTANT]
> Le SERVICE_NO_RESTART_WARNING _ulFlags_ peut ne pas être défini dans le fichier d’en-tête téléchargeable que vous avez actuellement, auquel cas vous pouvez l’ajouter à votre code à l’aide de la valeur suivante : `#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI utilise la méthode **IMsgServiceAdmin::CreateMsgService** pour ajouter un service à un profil. |

## <a name="see-also"></a>Voir aussi

[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
 [MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
