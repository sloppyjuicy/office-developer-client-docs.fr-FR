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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9f2ec8f0ec00f7314982e9b112415f69901c358c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424118"
---
# <a name="mapilogonex"></a>MAPILogonEx

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Connecte une application cliente à une session avec le système de messagerie. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix.h  <br/> |
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
  
> [in] Handle vers la fenêtre à laquelle la boîte de dialogue d’ouverture de conversation est modale. Si aucune boîte de dialogue n’apparaît pendant l’appel, le  _paramètre ulUIParam_ est ignoré. Ce paramètre peut être zéro. 
    
 _lpszProfileName_
  
> [in] Pointeur vers une chaîne qui contient le nom du profil à utiliser lorsque l’utilisateur se connecte. Cette chaîne est limitée à 64 caractères.
    
 _lpszPassword_
  
> [in] Pointeur vers une chaîne qui contient le mot de passe du profil. Le  _paramètre lpszPassword_ doit être NULL. 
    
 _flFlags_
  
> [in] Masque de bits d’indicateurs utilisés pour contrôler l’utilisation de la logon. Les indicateurs suivants peuvent être définies :
    
MAPI_ALLOW_OTHERS 
  
> La session partagée doit être renvoyée, ce qui permet aux clients ultérieurs d’obtenir la session sans fournir d’informations d’identification utilisateur. 
    
MAPI_BG_SESSION
  
> Connectez-vous à une session et exécutez toutes les opérations en arrière-plan. En règle générale, si un client a l’intention de traiter sur un thread d’arrière-plan ou dans un processus distinct d’une manière qui n’est pas discrète du thread au premier plan, il doit appeler avec l’indicateur MAPI_BG_SESSION. Une application cliente telle qu’un moteur d’indexation ou l’ouverture d’un fichier de dossiers personnels (PST) pour l’accès au type en arrière-plan sont quelques exemples d’utilisation de MAPI_BG_SESSION. MAPILogonEx.
    
MAPI_EXPLICIT_PROFILE 
  
> Le profil par défaut ne doit pas être utilisé et l’utilisateur doit être tenu de fournir un profil. 
    
MAPI_EXTENDED 
  
> Connectez-vous avec des fonctionnalités étendues. Cet indicateur doit toujours être définie.
    
MAPI_FORCE_DOWNLOAD 
  
> Une tentative doit être réalisée pour télécharger tous les messages de l’utilisateur avant de le renvoyer. Si l’MAPI_FORCE_DOWNLOAD n’est pas définie, les messages peuvent être téléchargés en arrière-plan après le retour de l’appel à MAPILogonEx. 
    
MAPI_LOGON_UI 
  
> Une boîte de dialogue doit s’afficher pour permettre à l’utilisateur d’obtenir des informations d’accès si nécessaire. Lorsque l’indicateur MAPI_LOGON_UI n’est pas définie, le client appelant n’affiche pas de boîte de dialogue de session et renvoie une valeur d’erreur si l’utilisateur n’est pas connecté.
    
MAPI_NEW_SESSION 
  
> Une tentative doit être réalisée pour créer une nouvelle session MAPI au lieu d’acquérir la session partagée. Si l’MAPI_NEW_SESSION n’est pas définie, MAPILogonEx utilise une session partagée existante, même si le paramètre  _lpszprofileName_ n’est pas NULL. 
    
MAPI_NO_MAIL 
  
> MAPI ne doit pas informer lepooler MAPI de l’existence de la session. Le résultat est qu’aucun message ne peut être envoyé ou reçu dans la session, sauf par le biais d’une paire de transport et de magasin étroitement couplée. Un client appelant définit cet indicateur s’il agit en tant qu’agent, si un travail de configuration doit être effectué ou si le client parcourant les magasins de messages disponibles. 
    
MAPI_NT_SERVICE 
  
> L’appelant s’exécute en tant que service Windows. Les appelants qui ne sont pas en cours d’exécution en tant que service Windows ne doivent pas définir cet indicateur . les appelants qui s’exécutent en tant que service doivent définir cet indicateur. 
    
MAPI_SERVICE_UI_ALWAYS 
  
> MAPILogonEx doit afficher une boîte de dialogue de configuration pour chaque service de message dans le profil. Les boîtes de dialogue s’affichent une fois que le profil a été choisi, mais avant qu’un service de message ne soit connecté. La boîte de dialogue COMMUNE MAPI pour l’ouverture de conversation contient également une case à cocher qui demande la même opération. 
    
MAPI_TIMEOUT_SHORT 
  
> L’accès doit échouer s’il est bloqué pendant plus de quelques secondes. 
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
MAPI_USE_DEFAULT 
  
> Le sous-système de messagerie doit remplacer le nom de profil du profil par défaut par le paramètre _lpszProfileName._ L MAPI_EXPLICIT_PROFILE est ignoré, sauf  _si lpszProfileName_ est NULL ou vide. 
    
 _lppSession_
  
> [out] Pointeur vers un pointeur vers l’interface de session MAPI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’logo a réussi.
    
MAPI_E_LOGON_FAILED 
  
> L’ouverture de session a échoué, soit parce qu’un ou plusieurs paramètres de MAPILogonEx n’étaient pas valides, soit parce qu’il y avait déjà trop de sessions ouvertes.
    
MAPI_E_TIMEOUT 
  
> MAPI sérialise toutes les connexions via un mutex. Elle est renvoyée si l’MAPI_TIMEOUT_SHORT a été définie et qu’un autre thread a maintenu le mutex. 
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération, généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Les applications clientes MAPI appellent la fonction MAPILogonEx pour se connecter à une session avec le système de messagerie. Toutes les chaînes transmises et renvoyées à et à partir d’appels MAPI sont terminées par null et doivent être spécifiées dans le jeu de caractères ou la page de code actuel du système d’exploitation du client ou du fournisseur appelant.
  
Le  _paramètre lpszProfileName_ est ignoré s’il existe une session précédente qui a appelé MapiLogonEx avec l’indicateur MAPI_ALLOW_OTHERS et si l’indicateur MAPI_NEW_SESSION n’est pas définie. Si le paramètre  _lpszProfileName_ a la valeur NULL ou pointe vers une chaîne vide et que le paramètre  _flFlags_ inclut l’indicateur MAPI_LOGON_UI, la fonction MAPILogonEx génère une boîte de dialogue d’accès avec un champ vide pour le nom du profil. 
  
Lors de la connexion à un profil spécifique, un client doit transmettre l’indicateur MAPI_NEW_SESSION mapiLogonEx en plus du nom de profil. Dans le cas contraire, si un autre client a établi une session partagée en se connectant avec MAPI_ALLOW_OTHERS, le client est connecté à la session partagée au lieu du profil demandé. 
  
L MAPI_EXPLICIT_PROFILE ne provoque pas l’utilisation du nom de profil par défaut lorsque  _lpszProfileName_ est NULL ou vide, sauf si l’indicateur MAPI_USE_DEFAULT est également présent. 
  
L MAPI_NO_MAIL’indicateur a plusieurs effets qui provoquent les effets suivants lorsque vous n’utilisez pas lepooler MAPI :
  
- Aucun message ne peut être envoyé ou remis par lepooler MAPI au cours de cette session. Seuls les fournisseurs de transport et de magasin étroitement couplés peuvent envoyer et remettre des messages. 
    
- Les magasins basés sur un serveur peuvent toujours envoyer ou remettre des messages. 
    
- Les messages envoyés ou remis par des magasins basés sur le serveur ne sont pas traitées par des fournisseurs de crochets. 
    
- Les options de transport par message et par destinataire ne sont pas disponibles. 
    
- La table d’état ne contient pas d’entrées pour les fournisseurs de transport et aucune fonctionnalité de transport dépendante des objets d’état (par exemple, la configuration) n’est disponible. 
    
- La ligne dupooler de message dans la table d’état contient la STATUS_FAILURE valeur. 
    
- Les connexions pibacked sont autorisées, mais ces connexions n’entraînent pas la réception des mises à jour de l’objet d’état par la connexion précédente. 
    
Un service doit toujours se connecter à l’aide de l MAPI_NO_MAIL de connexion. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::MAPILogonEx  <br/> |MFCMAPI utilise la méthode MAPILogonEx pour se connecter à MAPI.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

