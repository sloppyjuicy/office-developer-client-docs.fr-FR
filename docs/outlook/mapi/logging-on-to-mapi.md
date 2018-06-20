---
title: Se connecter à MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 05bafe43-a78a-4659-92f0-0b4fe444c64f
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 1ae3c47964ff238f57e98e0005a966008192f7c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784542"
---
# <a name="logging-on-to-mapi"></a>Se connecter à MAPI
 
**S’applique à**: Outlook 
  
Applications clientes ouvrez une session le sous-système MAPI en appelant la fonction **MAPILogonEx** . Pour plus d’informations, voir [MAPILogonEx](mapilogonex.md). **MAPILogonEx** valide la sélection de profil et la configuration de chaque fournisseur de services dans le profil. Une fois configuré, MAPI démarre les fournisseurs de carnet d’adresses avant de commencer les fournisseurs de banque de messages. Fournisseurs de transport sont démarrés lorsque leurs services sont d’abord requis. 
  
## <a name="choose-a-profile"></a>Choisir un profil
  
- Passer une chaîne de caractères qui représente le nom du profil dans le paramètre _lpszProfileName_ à **MAPILogonEx**, ou...
    
- Autorise l’utilisateur à spécifier le profil en transmettant la valeur NULL dans le paramètre _lpszProfileName_ et en définissant l’indicateur MAPI_LOGON_UI, ou... 

- Sélectionnez le profil par défaut en passant NULL dans le paramètre _lpszProfileName_ et en définissant l’indicateur MAPI_USE_DEFAULT. 
    
Si vous avez besoin d’un profil spécifique autre que le profil par défaut, vous devez enregistrer son nom dans votre propre base de données de configuration ou utiliser une convention d’affectation de noms spécifique. MAPI n’expose pas les attributs de profil autre que l’indicateur de nom et la valeur par défaut dans le tableau de profil et l’indicateur de profil par défaut est réservé pour la messagerie client et les applications associées IPM.
  
Clients qui fournissent le profil partiel ou les informations de configuration de fournisseur pour **MAPILogonEx** doivent demander à l’utilisateur pour les données supplémentaires en permettant à une boîte de dialogue s’affiche. Si les informations sont manquantes et **MAPILogonEx** ne peut pas demander à l’utilisateur de lui, l’ouverture de session échoue. Les clients qui ne pas besoin de l’entrée d’utilisateur peuvent supprimer l’affichage de boîte de dialogue. 
  
Les indicateurs **MAPILogonEx** utilise pour activer une interface utilisateur sont mutuellement ; seul peut être défini. En laissant ces indicateurs Annuler supprime l’affichage de l’interface utilisateur, à l’origine de **MAPILogonEx** échoue si les informations nécessaires sont manquantes. Autrement dit, si vous désactivez l’interface utilisateur et passez la valeur NULL pour le paramètre _lpszProfileName_ et que vous ne définissez pas l’indicateur MAPI_USE_DEFAULT, **MAPILogonEx** échoue parce qu’il ne peut pas récupérer un nom de profil. 
  
La session **MAPILogonEx** établit peut être une session non-messagerie, une session de messagerie partagée ou une session de messagerie spécifique. Sessions de messagerie individuelles sont des connexions entre votre client et le sous-système MAPI et peuvent être établies en définissant l’indicateur MAPI_NEW_SESSION dans l’appel de **MAPILogonEx**.
  
Sessions de messagerie partagées sont des connexions de plusieurs clients de messagerie peuvent utiliser. Les sessions partagées sont généralement définies pour les clients utilisent le même profil. Pour établir une nouvelle session en tant qu’une session partagée, définir l’indicateur MAPI_ALLOW_OTHERS. 
  
## <a name="use-an-existing-shared-session"></a>Utilisez une session partagée
  
- Ne définissez pas l’indicateur MAPI_NEW_SESSION.
    
- Ne définissez pas l’indicateur MAPI_ALLOW_OTHERS.
    
- Passez la valeur NULL pour le paramètre _lpszProfileName_ . 
    
- Passez la valeur NULL pour le paramètre _lpszPassword_ . 
    
Sessions non-messagerie permettent aux clients d’accéder à du sous-système MAPI, mais ne pas autorisent les messages envoyés ou reçus. Configuration ou l’administration des applications sont des exemples de clients qui devront d’établir des sessions non-messagerie. Pour demander une session non-messagerie, définir l’indicateur MAPI_NO_MAIL. Définition de cet indicateur connecte votre client sans en informer le spouleur MAPI. Les clients qui se connectent à MAPI avec cet indicateur ne peut pas s’attendent jamais recevoir des rapports d’état de lecture.
  
L’indicateur MAPI_NO_MAIL doit uniquement être définie :
  
- Si votre client ne sera pas envoyer ou recevoir des messages pendant la session.
    
- Si votre client possède le contrôle total sur le contenu du profil et les messages envoyés et reçus à l’aide d’étroitement couplés banque de messages et fournisseurs, tels que les fournisseurs de Microsoft Exchange de transport.
    
Un client de messagerie peut partager une session avec un client non-messagerie. Les caractéristiques d’un membre d’une session partagée ne sont pas affectés par les caractéristiques d’autres membres. Autrement dit, si vous ouvrez une session avec l’ensemble d’indicateurs MAPI_NO_MAIL et MAPI_ALLOW_OTHERS, se connecter à votre session d’un client de messagerie n’a aucun effet sur le fonctionnement de votre client, et inversement. Le client de messagerie sera toujours en mesure d’envoyer et recevoir des messages et votre client ne le pourront pas.
  
**MAPILogonEx** définit quelques autres indicateurs que vous pouvez définir : 
  
- MAPI_FORCE_DOWNLOAD indique que les messages entrants doivent être téléchargées avant **MAPILogonEx** renvoie. Ne pas cet indicateur provoque messages à télécharger en arrière-plan à une date ultérieure. 
    
- MAPI_SERVICE_UI_ALWAYS demande que chaque service de message dans le profil d’afficher une boîte de dialogue de configuration.
    
- MAPI_NT_SERVICE indique que votre client est implémentée comme un service Windows. Cet indicateur doit être défini si votre client est un service.
    
À chaque ouverture de session réussie, **MAPILogonEx** retourne un pointeur vers une session MAPI. Vous pouvez utiliser ce pointeur pour appeler les méthodes de l’interface **IMAPISession** . Pour plus d’informations, voir [IMAPISession : IUnknown](imapisessioniunknown.md). Pointeurs de session, quel que soit le type de session, sont uniques pour les clients qui les reçoivent et ne sont pas valides entre les tâches.
  

