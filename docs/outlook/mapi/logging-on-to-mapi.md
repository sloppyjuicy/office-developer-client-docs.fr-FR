---
title: Connexion à MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 05bafe43-a78a-4659-92f0-0b4fe444c64f
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: cce43301ac73a5646e263b2ab92700e57804637d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307776"
---
# <a name="logging-on-to-mapi"></a>Connexion à MAPI
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes se connectent au sous-système MAPI en appelant la fonction **MAPILogonEx** . Pour plus d'informations, consultez la rubrique [MAPILogonEx](mapilogonex.md). **MAPILogonEx** valide la sélection de profil et la configuration de chaque fournisseur de services dans le profil. Une fois configuré, MAPI démarre les fournisseurs de carnets d'adresses avant de démarrer les fournisseurs de banques de messages. Les fournisseurs de transport sont démarrés lorsque leurs services sont requis pour la première fois. 
  
## <a name="choose-a-profile"></a>Choisir un profil
  
- TransMettez une chaîne de caractères qui représente le nom du profil dans le paramètre _lpszProfileName_ à **MAPILogonEx**, ou...
    
- Autoriser l'utilisateur à spécifier le profil en passant NULL dans le paramètre _lpszProfileName_ et en définissant l'indicateur MAPI_LOGON_UI, ou... 

- Sélectionnez le profil par défaut en transmettant NULL dans le paramètre _lpszProfileName_ et en définissant l'indicateur MAPI_USE_DEFAULT. 
    
Si vous avez besoin d'un profil spécifique autre que le profil par défaut, vous devez enregistrer son nom dans votre propre base de données de configuration ou utiliser une convention d'affectation de noms spécifique. MAPI n'expose pas d'attributs de profil autres que le nom et l'indicateur par défaut dans la table de profils, et l'indicateur de profil par défaut est réservé pour le client de messagerie et les applications IPM associées.
  
Les clients qui fournissent des informations de configuration de fournisseur ou de profil partiel à **MAPILogonEx** doivent inviter l'utilisateur à entrer les données supplémentaires en autorisant l'affichage d'une boîte de dialogue. Si des informations sont manquantes et que **MAPILogonEx** ne peut pas inviter l'utilisateur à le fournir, la connexion échoue. Les clients qui n'ont pas besoin d'entrer l'utilisateur peuvent supprimer l'affichage de la boîte de dialogue. 
  
Les indicateurs utilisés par **MAPILogonEx** pour activer une interface utilisateur s'excluent mutuellement; une seule peut être définie. Le fait de ne pas affecter ces indicateurs supprime l'affichage d'une interface utilisateur, provoquant l'échec de **MAPILogonEx** si des informations nécessaires sont manquantes. Autrement dit, si vous désactivez l'interface utilisateur et transmettez la valeur NULL pour le paramètre _lpszProfileName_ et que vous ne définissez pas l'indicateur MAPI_USE_DEFAULT, **MAPILogonEx** échoue car il ne peut pas récupérer un nom de profil. 
  
La session que **MAPILogonEx** établit peut être une session de messagerie individuelle, une session de messagerie partagée ou une session de non-messagerie. Les sessions de messagerie individuelles sont des connexions privées entre votre client et le sous-système MAPI et peuvent être établies en définissant l'indicateur MAPI_NEW_SESSION dans l'appel à **MAPILogonEx**.
  
Les sessions de messagerie partagées sont des connexions que plusieurs clients de messagerie peuvent utiliser. Les sessions partagées sont généralement établies pour les clients qui utilisent le même profil. Pour établir une nouvelle session en tant que session partagée, définissez l'indicateur MAPI_ALLOW_OTHERS. 
  
## <a name="use-an-existing-shared-session"></a>Utiliser une session partagée existante
  
- Ne définissez pas l'indicateur MAPI_NEW_SESSION.
    
- Ne définissez pas l'indicateur MAPI_ALLOW_OTHERS.
    
- Transmettre NULL pour le paramètre _lpszProfileName_ . 
    
- Transmettre NULL pour le paramètre _lpszPassword_ . 
    
Les sessions non de messagerie permettent aux clients d'accéder au sous-système MAPI, mais n'autorisent pas l'envoi ou la réception de messages. Les applications de configuration ou d'administration sont des clients qui peuvent avoir besoin d'établir des sessions autres que des sessions de messagerie. Pour demander une session non de messagerie, définissez l'indicateur MAPI_NO_MAIL. La définition de cet indicateur déconnecte votre client sans informer le spouleur MAPI. Les clients qui se connectent à MAPI avec cet indicateur ne peuvent pas s'attendre à recevoir des rapports d'état de lecture.
  
L'indicateur MAPI_NO_MAIL doit être défini uniquement:
  
- Si votre client n'envoie pas ou ne reçoit pas de messages pendant la session.
    
- Si votre client dispose d'un contrôle total sur le contenu du profil et que les messages sont envoyés et reçus à l'aide de banques de messages et de fournisseurs de transport étroitement couplés, tels que les fournisseurs Microsoft Exchange.
    
Un client de messagerie peut partager une session avec un client non de messagerie. Les caractéristiques d'un membre d'une session partagée ne sont pas affectées par les caractéristiques d'autres membres. Autrement dit, si vous vous connectez avec les indicateurs MAPI_NO_MAIL et MAPI_ALLOW_OTHERS définis, un client de messagerie qui se connecte à votre session n'a aucun effet sur le fonctionnement de votre client et inversement. Le client de messagerie pourra toujours envoyer et recevoir des messages et votre client ne le sera pas.
  
**MAPILogonEx** définit quelques autres indicateurs que vous pouvez définir: 
  
- MAPI_FORCE_DOWNLOAD indique que les messages entrants doivent être téléchargés avant le renvoi de **MAPILogonEx** . Si vous ne définissez pas cet indicateur, les messages sont téléchargés en arrière-plan ultérieurement. 
    
- MAPI_SERVICE_UI_ALWAYS demande que chaque service de messagerie dans le profil affiche une boîte de dialogue de configuration.
    
- MAPI_NT_SERVICE indique que votre client est implémenté en tant que service Windows. Cet indicateur doit être défini si votre client est un service.
    
Avec chaque ouverture de session réussie, **MAPILogonEx** renvoie un pointeur vers une session MAPI. Vous pouvez utiliser ce pointeur pour appeler les méthodes de l'interface **IMAPISession** . Pour plus d'informations, consultez la rubrique [IMAPISession: IUnknown](imapisessioniunknown.md). Les pointeurs de session, quel que soit le type de session, sont propres aux clients qui les reçoivent et ne sont pas valides dans les tâches.
  

