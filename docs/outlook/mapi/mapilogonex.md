---
title: MAPILogonEx
description: Décrit la fonction MAPILogonEx et fournit la syntaxe, les paramètres, la valeur de retour, les remarques et la référence MFCMAPI.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPILogonEx
api_type:
- HeaderDef
ms.assetid: 98091e5b-1abd-4814-9c7a-583b420ee11d
ms.openlocfilehash: 0bdd0b08a562b8644b06c8a2251dcc4c29a710b0
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817052"
---
# <a name="mapilogonex"></a>MAPILogonEx

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Enregistre une application cliente sur une session avec le système de messagerie. 
  
|Propriété|Valeur|
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
  
> [in] Gérer jusqu’à la fenêtre dans laquelle la boîte de dialogue d’ouverture de session est modale. Si aucune boîte de dialogue n’apparaît pendant l’appel, le paramètre  _ulUIParam_ est ignoré. Ce paramètre peut être égal à zéro. 
    
 _lpszProfileName_
  
> [in] Pointeur vers une chaîne qui contient le nom du profil à utiliser lorsque l’utilisateur se connecte. Cette chaîne est limitée à 64 caractères.
    
 _lpszPassword_
  
> [in] Pointeur vers une chaîne qui contient le mot de passe du profil. Le paramètre  _lpszPassword_ doit être NULL. 
    
 _flFlags_
  
> [in] Masque de bits des indicateurs utilisés pour contrôler la façon dont l’ouverture de session est effectuée. Les indicateurs suivants peuvent être définis :
    
MAPI_ALLOW_OTHERS 
  
> La session partagée doit être retournée, ce qui permet aux clients ultérieurs d’obtenir la session sans fournir d’informations d’identification utilisateur. 
    
MAPI_BG_SESSION
  
> Connectez-vous à une session et exécutez toutes les opérations en arrière-plan. En général, si un client a l’intention d’effectuer un traitement sur un thread d’arrière-plan ou dans un processus distinct d’une manière qui n’est pas discrète pour le thread de premier plan, il doit appeler avec l’indicateur MAPI_BG_SESSION. Une application cliente telle qu’un moteur d’indexation ou l’ouverture d’un fichier de dossiers personnels (PST) pour l’accès au type d’arrière-plan sont quelques exemples d’emplacement où utiliser MAPI_BG_SESSION. MAPILogonEx.
    
MAPI_EXPLICIT_PROFILE 
  
> Le profil par défaut ne doit pas être utilisé et l’utilisateur doit être tenu de fournir un profil. 
    
MAPI_EXTENDED 
  
> Connectez-vous avec des fonctionnalités étendues. Cet indicateur doit toujours être défini.
    
MAPI_FORCE_DOWNLOAD 
  
> Une tentative doit être effectuée pour télécharger tous les messages de l’utilisateur avant de revenir. Si l’indicateur MAPI_FORCE_DOWNLOAD n’est pas défini, les messages peuvent être téléchargés en arrière-plan après le retour de l’appel à MAPILogonEx. 
    
MAPI_LOGON_UI 
  
> Une boîte de dialogue doit s’afficher pour inviter l’utilisateur à entrer des informations d’ouverture de session si nécessaire. Lorsque l’indicateur MAPI_LOGON_UI n’est pas défini, le client appelant n’affiche pas de boîte de dialogue d’ouverture de session et retourne une valeur d’erreur si l’utilisateur n’est pas connecté.
    
MAPI_NEW_SESSION 
  
> Une tentative doit être effectuée pour créer une session MAPI au lieu d’acquérir la session partagée. Si l’indicateur MAPI_NEW_SESSION n’est pas défini, MAPILogonEx utilise une session partagée existante, même si le paramètre _lpszprofileName_ n’est pas NULL. 
    
MAPI_NO_MAIL 
  
> MAPI ne doit pas informer le spouleur MAPI de l’existence de la session. Le résultat est qu’aucun message ne peut être envoyé ou reçu dans la session, à l’exception d’une paire de stockage et de transport étroitement couplée. Un client appelant définit cet indicateur s’il agit en tant qu’agent, si le travail de configuration doit être effectué ou si le client parvient à parcourir les magasins de messages disponibles. 
    
MAPI_NT_SERVICE 
  
> L’appelant s’exécute en tant que service Windows. Les appelants qui ne s’exécutent pas en tant que service Windows ne doivent pas définir cet indicateur ; les appelants qui s’exécutent en tant que service doivent définir cet indicateur. 
    
MAPI_SERVICE_UI_ALWAYS 
  
> MAPILogonEx doit afficher une boîte de dialogue de configuration pour chaque service de message dans le profil. Les boîtes de dialogue s’affichent une fois que le profil a été choisi, mais avant que n’importe quel service de message soit connecté. La boîte de dialogue commune MAPI pour l’ouverture de session contient également une case à cocher qui demande la même opération. 
    
MAPI_TIMEOUT_SHORT 
  
> L’ouverture de session doit échouer si elle est bloquée pendant plus de quelques secondes. 
    
MAPI_UNICODE 
  
> Les chaînes passées sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, les chaînes sont au format ANSI. 
    
MAPI_USE_DEFAULT 
  
> Le sous-système de messagerie doit remplacer le nom du profil par défaut par le paramètre  _lpszProfileName_ . L’indicateur MAPI_EXPLICIT_PROFILE est ignoré, sauf si  _lpszProfileName_ est NULL ou vide. 
    
 _lppSession_
  
> [out] Pointeur vers un pointeur vers l’interface de session MAPI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’ouverture de session a réussi.
    
MAPI_E_LOGON_FAILED 
  
> L’ouverture de session a échoué, soit parce qu’un ou plusieurs des paramètres de MAPILogonEx n’étaient pas valides, soit parce qu’il y avait déjà trop de sessions ouvertes.
    
MAPI_E_TIMEOUT 
  
> MAPI sérialise tous les logons via un mutex. Cette valeur est retournée si l’indicateur MAPI_TIMEOUT_SHORT a été défini et qu’un autre thread a conservé le mutex. 
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération, généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Les applications clientes MAPI appellent la fonction MAPILogonEx pour se connecter à une session avec le système de messagerie. Toutes les chaînes transmises et retournées vers et à partir d’appels MAPI sont terminées par une valeur Null et doivent être spécifiées dans le jeu de caractères ou la page de codes actuels du client appelant ou du système d’exploitation du fournisseur.
  
Le paramètre  _lpszProfileName_ est ignoré s’il existe une session précédente qui a appelé MapiLogonEx avec l’indicateur MAPI_ALLOW_OTHERS défini et si l’indicateur MAPI_NEW_SESSION n’est pas défini. Si le paramètre  _lpszProfileName_ a la valeur NULL ou pointe vers une chaîne vide et que le paramètre  _flFlags_ inclut l’indicateur MAPI_LOGON_UI, la fonction MAPILogonEx génère une boîte de dialogue d’ouverture de session avec un champ vide pour le nom du profil. 
  
Lors de la connexion à un profil spécifique, un client doit transmettre l’indicateur MAPI_NEW_SESSION dans MAPILogonEx en plus du nom du profil. Sinon, si un autre client a établi une session partagée en se connectant avec MAPI_ALLOW_OTHERS, le client est connecté à la session partagée au lieu du profil demandé. 
  
L’indicateur MAPI_EXPLICIT_PROFILE n’entraîne pas l’utilisation du nom de profil par défaut lorsque  _lpszProfileName_ est NULL ou vide, sauf si l’indicateur de MAPI_USE_DEFAULT est également présent. 
  
L’indicateur MAPI_NO_MAIL a plusieurs effets qui provoquent ce qui suit quand vous n’utilisez pas le spouleur MAPI :
  
- Aucun message ne peut être envoyé ou remis par le spouleur MAPI pendant cette session. Seuls les fournisseurs de stockage et de transport étroitement couplés peuvent envoyer et remettre des messages. 
    
- Les magasins basés sur le serveur peuvent toujours envoyer ou remettre des messages. 
    
- Les messages envoyés ou remis par les magasins basés sur le serveur ne sont traités par aucun fournisseur hook. 
    
- Les options par message et par destinataire pour les transports ne sont pas disponibles. 
    
- La table d’état ne contient pas d’entrées pour les fournisseurs de transport, et aucune fonctionnalité de transport dépendante des objets d’état (comme la configuration) n’est disponible. 
    
- La ligne du spouleur de message dans la table d’état contient la valeur STATUS_FAILURE. 
    
- Les journaux d’activité avec ouverture de session sont autorisés, mais ces journaux n’entraînent pas la réception des mises à jour de l’objet d’état par l’ouverture de session précédente. 
    
Un service doit toujours se connecter à l’aide de l’indicateur MAPI_NO_MAIL. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::MAPILogonEx  <br/> |MFCMAPI utilise la méthode MAPILogonEx pour se connecter à MAPI. |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

