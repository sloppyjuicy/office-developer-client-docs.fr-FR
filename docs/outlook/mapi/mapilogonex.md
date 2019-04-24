---
title: MAPILogonEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPILogonEx
api_type:
- HeaderDef
ms.assetid: 98091e5b-1abd-4814-9c7a-583b420ee11d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9f2ec8f0ec00f7314982e9b112415f69901c358c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346647"
---
# <a name="mapilogonex"></a>MAPILogonEx

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Enregistre une application cliente sur une session avec le système de messagerie. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> dans Handle vers la fenêtre dans laquelle la boîte de dialogue d'ouverture de session est modale. Si aucune boîte de dialogue ne s'affiche lors de l'appel, le paramètre _ulUIParam_ est ignoré. Ce paramètre peut être égal à zéro. 
    
 _lpszProfileName_
  
> dans Pointeur vers une chaîne qui contient le nom du profil à utiliser lorsque l'utilisateur se connecte. Cette chaîne est limitée à 64 caractères.
    
 _lpszPassword_
  
> dans Pointeur vers une chaîne qui contient le mot de passe du profil. Le paramètre _lpszPassword_ doit être null. 
    
 _flFlags_
  
> dans Masque de des indicateurs utilisés pour contrôler le mode d'ouverture de session. Les indicateurs suivants peuvent être définis:
    
MAPI_ALLOW_OTHERS 
  
> La session partagée doit être renvoyée, ce qui permet aux clients ultérieurs d'obtenir la session sans fournir d'informations d'identification d'utilisateur. 
    
MAPI_BG_SESSION
  
> Ouvrez une session sur une session et exécutez les opérations en arrière-plan. En général, si un client envisage d'effectuer un traitement sur un thread d'arrière-plan ou dans un processus distinct d'une manière qui n'est pas gênante pour le thread de premier plan, il doit appeler avec l'indicateur MAPI_BG_SESSION. Une application cliente, telle qu'un moteur d'indexation ou l'ouverture d'un fichier de dossiers personnels (PST) pour l'accès aux types d'arrière-plan est un exemple d'emplacement où utiliser MAPI_BG_SESSION. MAPILogonEx.
    
MAPI_EXPLICIT_PROFILE 
  
> Le profil par défaut ne doit pas être utilisé et l'utilisateur doit être obligé de fournir un profil. 
    
MAPI_EXTENDED 
  
> Ouvrez une session avec des fonctionnalités étendues. Cet indicateur doit toujours être défini.
    
MAPI_FORCE_DOWNLOAD 
  
> Une tentative de téléchargement de tous les messages de l'utilisateur est effectuée avant de renvoyer. Si l'indicateur MAPI_FORCE_DOWNLOAD n'est pas défini, les messages peuvent être téléchargés en arrière-plan après l'appel de MAPILogonEx. 
    
MAPI_LOGON_UI 
  
> Une boîte de dialogue doit s'afficher pour inviter l'utilisateur à entrer des informations de connexion si nécessaire. Lorsque l'indicateur MAPI_LOGON_UI n'est pas défini, le client appelant n'affiche pas de boîte de dialogue d'ouverture de session et renvoie une valeur d'erreur si l'utilisateur n'est pas connecté.
    
MAPI_NEW_SESSION 
  
> Une tentative de création d'une session MAPI doit être effectuée au lieu d'acquérir la session partagée. Si l'indicateur MAPI_NEW_SESSION n'est pas défini, MAPILogonEx utilise une session partagée existante même si le paramètre _lpszprofileName_ n'est pas null. 
    
MAPI_NO_MAIL 
  
> MAPI ne doit pas informer le spouleur MAPI de l'existence de la session. Le résultat est qu'aucun message ne peut être envoyé ou reçu dans la session, sauf via un magasin et une paire de transport étroitement couplés. Un client appelant définit cet indicateur s'il agit comme un agent, si le travail de configuration doit être réalisé ou si le client parcourt les banques de messages disponibles. 
    
MAPI_NT_SERVICE 
  
> L'appelant est exécuté en tant que service Windows. Les appelants qui ne s'exécutent pas en tant que service Windows ne doivent pas définir cet indicateur; les appelants qui s'exécutent en tant que service doivent définir cet indicateur. 
    
MAPI_SERVICE_UI_ALWAYS 
  
> MAPILogonEx doit afficher une boîte de dialogue de configuration pour chaque service de messagerie dans le profil. Les boîtes de dialogue s'affichent après que le profil a été choisi mais avant qu'un service de messagerie ne soit connecté. La boîte de dialogue commune MAPI pour l'ouverture de session contient également une case à cocher qui demande la même opération. 
    
MAPI_TIMEOUT_SHORT 
  
> La connexion doit échouer si elle est bloquée pendant plus de quelques secondes. 
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI. 
    
MAPI_USE_DEFAULT 
  
> Le sous-système de messagerie doit remplacer le nom de profil du profil par défaut pour le paramètre _lpszProfileName_ . L'indicateur MAPI_EXPLICIT_PROFILE est ignoré à moins que _lpszProfileName_ soit null ou vide. 
    
 _lppSession_
  
> remarquer Pointeur vers un pointeur vers l'interface de session MAPI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'ouverture de session a réussi.
    
MAPI_E_LOGON_FAILED 
  
> L'ouverture de session a échoué, car un ou plusieurs paramètres de MAPILogonEx étaient incorrects ou des sessions ont déjà été ouvertes.
    
MAPI_E_TIMEOUT 
  
> MAPI sérialise toutes les ouvertures de sessions via un mutex. Cette valeur est renvoyée si l'indicateur MAPI_TIMEOUT_SHORT a été défini et qu'un autre thread a maintenu le mutex. 
    
MAPI_E_USER_CANCEL 
  
> L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton **Annuler** d'une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Les applications clientes MAPI appellent la fonction MAPILogonEx pour se connecter à une session avec le système de messagerie. Toutes les chaînes transmises et renvoyées vers et à partir des appels MAPI sont terminées par un caractère null et doivent être spécifiées dans le jeu de caractères ou la page de codes actuelle du système d'exploitation du client ou du fournisseur appelant.
  
Le paramètre _lpszProfileName_ est ignoré s'il existe une session précédente qui a appelé MAPILogonEx avec l'indicateur MAPI_ALLOW_OTHERS défini et si l'indicateur MAPI_NEW_SESSION n'est pas défini. Si le paramètre _lpszProfileName_ est null ou pointe vers une chaîne vide et que le paramètre _flFlags_ inclut l'indicateur MAPI_LOGON_UI, la fonction MAPILogonEx génère une boîte de dialogue de connexion dont le nom de profil est vide. 
  
Lors de la connexion à un profil spécifique, un client doit transmettre l'indicateur MAPI_NEW_SESSION dans MAPILogonEx en plus du nom du profil. Dans le cas contraire, si un autre client a établi une session partagée en se connectant avec MAPI_ALLOW_OTHERS, le client sera connecté à la session partagée au lieu de s'ouvrir sur le profil demandé. 
  
L'indicateur MAPI_EXPLICIT_PROFILE n'entraîne pas l'utilisation du nom de profil par défaut lorsque _lpszProfileName_ est null ou vide, sauf si l'indicateur MAPI_USE_DEFAULT est également présent. 
  
L'indicateur MAPI_NO_MAIL a plusieurs effets qui provoquent ce qui suit lorsque vous n'utilisez pas le spouleur MAPI:
  
- Aucun message ne peut être envoyé ou remis par le spouleur MAPI au cours de cette session. Seuls les fournisseurs de banque et de transport étroitement couplés peuvent envoyer et livrer des messages. 
    
- Les magasins basés sur un serveur peuvent toujours envoyer ou renvoyer des messages. 
    
- Les messages envoyés ou remis par des magasins basés sur un serveur ne sont pas traités par les fournisseurs de Hook. 
    
- Les options par message et par destinataire pour les transports ne sont pas disponibles. 
    
- La table d'État ne contient pas d'entrées pour les fournisseurs de transport et les fonctionnalités de transport dépendantes des objets d'État (telles que la configuration) ne sont pas disponibles. 
    
- La ligne message Spooler de la table d'état contient la valeur STATUS_FAILURE. 
    
- Les ouvertures de sessions superposes sont autorisées, mais ces ouvertures de session ne provoquent pas la réception des mises à jour de l'objet d'État par la connexion précédente. 
    
Un service doit toujours se connecter à l'aide de l'indicateur MAPI_NO_MAIL. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIObjects. cpp  <br/> |CMapiObjects:: MAPILogonEx  <br/> |MFCMAPI utilise la méthode MAPILogonEx pour se connecter à MAPI.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

