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
ms.openlocfilehash: 08782fe616fe260388cff8982dfbb09951453a00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784739"
---
# <a name="mapilogonex"></a>MAPILogonEx

  
  
**S’applique à**: Outlook 
  
Enregistre une application client à une session avec le système de messagerie. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIX.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
   
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
  
> [in] Handle vers la fenêtre à laquelle la boîte de dialogue d’ouverture de session est modale. Si aucune boîte de dialogue s’affiche lors de l’appel, le paramètre _ulUIParam_ est ignoré. Ce paramètre peut être égal à zéro. 
    
 _lpszProfileName_
  
> [in] Pointeur vers une chaîne qui contient le nom du profil à utiliser lors de l’utilisateur se connecte. Cette chaîne est limitée à 64 caractères.
    
 _lpszPassword_
  
> [in] Pointeur vers une chaîne qui contient le mot de passe du profil. Le paramètre _lpszPassword_ doit être NULL. 
    
 _flFlags_
  
> [in] Masque de bits d’indicateurs utilisés pour contrôler la façon dont l’ouverture de session est effectuée. Les indicateurs suivants peuvent être définis :
    
MAPI_ALLOW_OTHERS 
  
> La session partagée doit être retournée, qui permet une version ultérieure aux clients d’obtenir la session sans fournir les informations d’identification de l’utilisateur. 
    
MAPI_BG_SESSION
  
> Ouvrez une session et exécuter des opérations en arrière-plan. En règle générale, si un client a l’intention d’effectuer un traitement sur une thread d’arrière-plan ou dans un processus distinct d’une manière discrète à la thread de premier plan, il doit appeler avec l’indicateur MAPI_BG_SESSION. Une application cliente comme un moteur d’indexation ou de l’ouverture d’un fichier de dossiers personnels (PST) pour l’accès de type d’arrière-plan sont des exemples d’utilisation de MAPI_BG_SESSION. MAPILogonEx.
    
MAPI_EXPLICIT_PROFILE 
  
> Le profil par défaut ne doit pas être utilisé et que l’utilisateur doit être nécessaire de fournir un profil. 
    
MAPI_EXTENDED 
  
> Ouvrez une session avec des capacités étendues. Cet indicateur doit toujours être défini.
    
MAPI_FORCE_DOWNLOAD 
  
> Une tentative doit être effectuée pour télécharger tous les messages de l’utilisateur avant de renvoyer. Si l’indicateur MAPI_FORCE_DOWNLOAD n’est pas définie, les messages peuvent être téléchargés en arrière-plan après l’appel à MAPILogonEx. 
    
MAPI_LOGON_UI 
  
> Une boîte de dialogue doit être affichée pour demander à l’utilisateur pour les informations de connexion si nécessaire. Lorsque l’indicateur MAPI_LOGON_UI n’est pas défini, le client appelant n’affiche pas une boîte de dialogue d’ouverture de session et renvoie une valeur d’erreur si l’utilisateur n’est pas connecté.
    
MAPI_NEW_SESSION 
  
> Une tentative doit être effectuée pour créer une nouvelle session MAPI au lieu de l’acquisition de la session partagée. Si l’indicateur MAPI_NEW_SESSION n’est pas définie, MAPILogonEx utilise une session partagée, même si le paramètre _lpszprofileName_ n’est pas NULL. 
    
MAPI_NO_MAIL 
  
> MAPI ne doit pas informer le spouleur MAPI de l’existence de la session. Le résultat est qu’aucun message peut être envoyé ou reçu dans la session sauf via étroitement couplés stocker et paire de transport. Un client appelant définit cet indicateur si elle agit comme un agent, si le travail de configuration doit être effectuée, ou si le client parcourt les banques de messages disponibles. 
    
MAPI_NT_SERVICE 
  
> L’appelant est exécuté comme un service Windows. Appelants qui n’exécutent pas comme un service Windows ne doit pas définir cet indicateur ; Cet indicateur doivent être défini par les appelants qui sont en cours d’exécution en tant que service. 
    
MAPI_SERVICE_UI_ALWAYS 
  
> MAPILogonEx doit afficher une boîte de dialogue de configuration pour chaque service de message dans le profil. Les boîtes de dialogue sont affichent une fois que le profil a été sélectionné mais avant tout message service est connecté. La boîte de dialogue commune MAPI pour l’ouverture de session contient également une case à cocher qui demande la même opération. 
    
MAPI_TIMEOUT_SHORT 
  
> L’ouverture de session doit échouer si bloqué pendant plus de quelques secondes. 
    
MAPI_UNICODE 
  
> Les chaînes passée sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
MAPI_USE_DEFAULT 
  
> Le sous-système de messagerie doit remplacer le nom de profil du profil par défaut pour le paramètre _lpszProfileName_ . L’indicateur MAPI_EXPLICIT_PROFILE est ignoré à moins que _lpszProfileName_ est NULL ou vide. 
    
 _lppSession_
  
> [out] Pointeur vers un pointeur vers l’interface de session MAPI.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La connexion a réussi.
    
MAPI_E_LOGON_FAILED 
  
> La connexion a échoué, car un ou plusieurs des paramètres MAPILogonEx ne sont pas valides ou trop de sessions étaient déjà ouvert.
    
MAPI_E_TIMEOUT 
  
> MAPI sérialise toutes les ouvertures de session via un mutex. Il est renvoyé si l’indicateur MAPI_TIMEOUT_SHORT a été défini et un autre thread détenus mutex. 
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Les applications clientes MAPI appellent la fonction MAPILogonEx pour vous connecter à une session avec le système de messagerie. Toutes les chaînes qui sont transmis et renvoyés vers et depuis les appels MAPI sont terminée et doivent être spécifiés dans le jeu de caractères en cours ou page du système d’exploitation client ou du fournisseur d’appel de code.
  
Le paramètre _lpszProfileName_ est ignoré s’il existe une session précédente existante qui a appelé MapiLogonEx avec l’indicateur MAPI_ALLOW_OTHERS et si l’indicateur MAPI_NEW_SESSION n’est pas définie. Si le paramètre _lpszProfileName_ est NULL ou pointe vers une chaîne vide et le paramètre _flFlags_ inclut l’indicateur MAPI_LOGON_UI, la fonction MAPILogonEx génère une boîte de dialogue d’ouverture de session qui a un champ vide pour le nom du profil. 
  
Lors de la connexion à un profil spécifique, un client doit passer l’indicateur MAPI_NEW_SESSION dans MAPILogonEx en plus du nom du profil. Dans le cas contraire, si un autre client a établi une session partagée en vous connectant avec MAPI_ALLOW_OTHERS, le client sera connecté en à la session partagée au lieu d’au profil demandé. 
  
L’indicateur MAPI_EXPLICIT_PROFILE pas provoquer le nom du profil par défaut à utiliser lorsque _lpszProfileName_ a la valeur NULL est vide ou ne, sauf si l’indicateur MAPI_USE_DEFAULT est également présent. 
  
L’indicateur MAPI_NO_MAIL a plusieurs effets provoquer ce qui suit lorsque vous n’utilisez ne pas le spouleur MAPI :
  
- Aucun message ne peut être envoyées ou transmis par le spouleur MAPI pendant cette session. Seuls fournisseurs de banque et de transport étroitement couplés peuvent envoyer et remettre des messages. 
    
- Magasins de serveur peuvent toujours envoyer ou remettre des messages. 
    
- Messages envoyés et remis par les magasins de serveur ne sont pas traitées par les fournisseurs de raccordement. 
    
- Options de chaque message et par destinataire pour des transports ne sont pas disponibles. 
    
- La table d’état ne contient-elle pas d’entrées pour les fournisseurs de transport et les fonctionnalités de transport dépendent d’objets d’état (par exemple, configuration) ne sont pas disponible. 
    
- La ligne dans la table d’état spouleur du message contient la valeur de la valeur. 
    
- Ouvertures de session superposables (piggyback) sont autorisés, mais les ouvertures de session ne provoquent pas l’ouverture de session précédente recevoir des mises à jour de statut objet. 
    
Un service doit toujours se connecter à l’aide de l’indicateur MAPI_NO_MAIL. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::MAPILogonEx  <br/> |MFCMAPI utilise la méthode MAPILogonEx pour se connecter à MAPI.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

