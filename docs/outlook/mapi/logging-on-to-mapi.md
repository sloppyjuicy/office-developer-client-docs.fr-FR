---
title: Connexion à MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 05bafe43-a78a-4659-92f0-0b4fe444c64f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: aa38ffd213b6ff7d2a9216d50350cf1d1fb7a037
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462889"
---
# <a name="logging-on-to-mapi"></a>Connexion à MAPI
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes se connectent au sous-système MAPI en appelant la **fonction MAPILogonEx** . Pour plus d’informations, [voir MAPILogonEx](mapilogonex.md). **MAPILogonEx valide** la sélection de profil et la configuration de chaque fournisseur de services dans le profil. Une fois configuré, MAPI démarre les fournisseurs de carnet d’adresses avant de démarrer les fournisseurs de magasins de messages. Les fournisseurs de transport sont démarrés lorsque leurs services sont requis pour la première fois. 
  
## <a name="choose-a-profile"></a>Choisir un profil
  
- Passez une chaîne de caractères qui représente le nom du profil dans le paramètre _lpszProfileName_ **à MAPILogonEx**, ou...
    
- Autorisez l’utilisateur à spécifier le profil en passant null dans le paramètre _lpszProfileName_ et en paramétifiant l’MAPI_LOGON_UI, ou... 

- Sélectionnez le profil par défaut en passant la valeur NULL dans le paramètre _lpszProfileName_ et en MAPI_USE_DEFAULT’indicateur. 
    
Si vous avez besoin d’un profil spécifique autre que le profil par défaut, vous devez enregistrer son nom dans votre propre base de données de configuration ou utiliser une convention d’attribution de noms spécifique. MAPI n’expose aucun attribut de profil autre que le nom et l’indicateur par défaut dans la table de profils, et l’indicateur de profil par défaut est réservé au client de messagerie et aux applications IPM associées.
  
Les clients qui fournissent des informations partielles sur la configuration du profil ou du fournisseur dans **MAPILogonEx** doivent fournir des données supplémentaires à l’utilisateur en permettant l’affichage d’une boîte de dialogue. Si des informations sont manquantes **et que MAPILogonEx ne** peut pas invite l’utilisateur à les fournir, l’accès échoue. Les clients qui n’ont pas besoin d’une entrée utilisateur peuvent supprimer l’affichage de la boîte de dialogue. 
  
Les indicateurs que **MAPILogonEx utilise** pour activer une interface utilisateur s’excluent mutuellement ; Un seul peut être définie. L’absence de ces indicateurs supprime l’affichage d’une interface utilisateur, ce qui entraîne l’échec de **MAPILogonEx** si des informations nécessaires sont manquantes. Autrement dit, si vous désactivez l’interface utilisateur et passez la valeur NULL pour le paramètre  _lpszProfileName_ et que vous ne définissez pas l’indicateur MAPI_USE_DEFAULT, **MAPILogonEx** échouera car il ne peut pas récupérer un nom de profil. 
  
La session que **MAPILogonEx** établit peut être une session de messagerie individuelle, une session de messagerie partagée ou une session de non-recherche. Les sessions de messagerie individuelles sont des connexions privées entre votre client et le sous-système MAPI et peuvent être établies en fixant l’indicateur MAPI_NEW_SESSION dans l’appel à **MAPILogonEx**.
  
Les sessions de messagerie partagées sont des connexions que plusieurs clients de messagerie peuvent utiliser. Les sessions partagées sont généralement établies pour les clients qui utilisent le même profil. Pour établir une nouvelle session en tant que session partagée, définissez l’MAPI_ALLOW_OTHERS de session. 
  
## <a name="use-an-existing-shared-session"></a>Utiliser une session partagée existante
  
- Ne définissez pas l’MAPI_NEW_SESSION de l’indicateur.
    
- Ne définissez pas l’MAPI_ALLOW_OTHERS de l’indicateur.
    
- Passez NULL pour le  _paramètre lpszProfileName_ . 
    
- Passez NULL pour le  _paramètre lpszPassword_ . 
    
Les sessions de non-recherche permettent aux clients d’accéder au sous-système MAPI, mais n’autorisent pas l’envoi ou la réception de messages. Les applications de configuration ou d’administration sont des exemples de clients qui peuvent avoir besoin d’établir des sessions de non-recherche. Pour demander une session de non-recherche, définissez l’MAPI_NO_MAIL de recherche. La définition de cet indicateur connecte votre client sans en informer lepooler MAPI. Les clients qui se connectent à MAPI avec cet indicateur ne peuvent pas s’attendre à recevoir des rapports d’état de lecture.
  
L MAPI_NO_MAIL de contrôle doit uniquement être définie :
  
- Si votre client n’envoie ou ne reçoit pas de messages pendant la session.
    
- Si votre client dispose d’un contrôle total sur le contenu du profil et que les messages sont envoyés et reçus à l’aide de fournisseurs de transport et de magasin de messages étroitement couplés, tels que les fournisseurs Microsoft Exchange.
    
Un client de messagerie peut partager une session avec un client qui n’est pas un client de recherche. Les caractéristiques d’un membre d’une session partagée ne sont pas affectées par les caractéristiques des autres membres. Autrement dit, si vous vous connectez avec les indicateurs MAPI_NO_MAIL et MAPI_ALLOW_OTHERS, une connexion du client de messagerie à votre session n’a aucune incidence sur le fonctionnement de votre client et inversement. Le client de messagerie sera toujours en mesure d’envoyer et de recevoir des messages, ce qui n’est pas le cas de votre client.
  
**MAPILogonEx** définit quelques autres indicateurs que vous pouvez définir : 
  
- MAPI_FORCE_DOWNLOAD indique que les messages entrants doivent être téléchargés avant le retour **de MAPILogonEx** . Le fait de ne pas définir cet indicateur entraîne le téléchargement ultérieur des messages en arrière-plan. 
    
- MAPI_SERVICE_UI_ALWAYS demande à chaque service de message du profil d’afficher une boîte de dialogue de configuration.
    
- MAPI_NT_SERVICE indique que votre client est implémenté en tant que service Windows client. Cet indicateur doit être définie si votre client est un service.
    
Avec chaque ouverture de session réussie, **MAPILogonEx renvoie** un pointeur vers une session MAPI. Vous pouvez utiliser ce pointeur pour appeler les méthodes de l’interface **IMAPISession** . Pour plus d’informations, [voir IMAPISession : IUnknown](imapisessioniunknown.md). Les pointeurs de session, quel que soit le type de session, sont propres aux clients qui les reçoivent et ne sont pas valides pour toutes les tâches.
  

