---
title: Sessions MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c5a7c137-393e-40ff-a2b9-afe02da2435a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a2ab44081c79e72e082687006ab06d0f83b8367e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575027"
---
# <a name="mapi-sessions"></a>Sessions MAPI

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Avant que l'application cliente peut appeler un syst�me de messagerie sous-jacent, il doit �tablir une connexion avec le sous-syst�me MAPI ou session.
  
Sessions are initiated when a user logs on, a process that accesses a valid profile and validates the messaging system and the message service credentials. Then, the process ensures that all of the profile's message services are correctly configured. The client interface you use determines the logon call. MAPI clients call the [MAPILogonEx](mapilogonex.md) function. 
  
Configuration du service de message est un des �l�ments plus importants du processus d'ouverture de session. Le profil est la source initiale pour les informations de configuration. Si les informations d'un service de message particulier sont absent, le processus d'ouverture de session tente de demander � l'utilisateur de lui. Cela n'est pas toujours r�ussie pour deux raisons : tout d'abord, inviter l'utilisateur requiert l'affichage d'une bo�te de dialogue. Il est possible pour les clients pour ne pas autoriser l'affichage de l'interface utilisateur en passant un indicateur � l'appel d'ouverture de session. Deuxi�mement, l'utilisateur peut annuler la bo�te de dialogue avant de pouvoir ajouter les informations n�cessaires.
  
Lorsqu'un processus d'ouverture de session �choue une fois, l'utilisateur est inform� de l'�chec et la possibilit� de recommencer ou corriger la condition d'erreur. Une fois encore, une interface utilisateur s'affichera, si le client lui permet, et l'utilisateur sera invit� � entrer les donn�es sont manquantes. Si ce bloc try deuxi�me �choue, MAPI d�sactive tous les fournisseurs de service dans le service de message pour la dur�e de la session. En effet, le service de l'ensemble du message est d�sactiv�. Cela signifie qu'aucun des fournisseurs de service dans le service de message peuvent travailler. Cette op�ration est effectu�e, car si le fournisseur d'un �chec d'ouverture de session, les autres fournisseurs g�n�ralement �galement �chouent. Le processus d'ouverture de session peut �chouer en raison d'un chemin d'acc�s non valide pour une ressource n�cessaire, une version incompatible de MAPI, un serveur de messagerie non disponible ou corruption des donn�es. 
  
Les clients peuvent sp�cifier un des deux types de sessions �tablies lors de l'appel d'ouverture de session : une session individuelle ou une session partag�e. Sessions individuelles sont les connexions priv�es ; Il existe une relation entre une application cliente et la session qu'il utilise. Par cons�quent, les applications clientes qui partagent une session �galement en partager un profil. Les sessions partag�es sont �tablies une seule fois, mais peuvent �tre utilis�es par d'autres applications client ayant besoin d'utiliser leur. Le profil et les informations d'identification sont sp�cifi�es uniquement avec les param�tres de connexion initiale. 
  
Clients peuvent ouvrir une session plusieurs fois en tant que le m�me utilisateur ou plusieurs utilisateurs. MAPI n'emp�che pas cela. Certains fournisseurs de services, cependant, peuvent ne pas �tre aussi souples, renvoient la valeur d'erreur MAPI_E_SESSION_LIMIT lors de tentatives de connexion ult�rieures. Fournisseurs de services avec des restrictions de mat�riel sous-jacent peuvent �tre n�cessaire pour appliquer une limite de session.
  
Les appels de fonction permettant d'�tablir une session poss�dent une collection de param�tres et des indicateurs qui contr�lent la cr�ation de la session. Le client sp�cifie un nom de profil facultatif et un handle de fen�tre qui sert � la fen�tre parent pour toutes les bo�tes de dialogue qui s'affichent. Les indicateurs incluent MAPI_NEW_SESSION, qui demande une nouvelle session individuelle (plut�t qu'une session partag�e) �tablis, et l'indicateur d'interface utilisateur MAPI_LOGON_UI. L'indicateur d'interface utilisateur est d�finie pour demander une bo�te de dialogue d'ouverture de session.
  
L'illustration suivante montre comment ces param�tres et des indicateurs diff�rents �tablissent une session MAPI.
  
**Diagramme de flux de session�MAPI**
  
![Organigramme de session MAPI] (media/amapi_47.gif "Organigramme de session MAPI")
  
For information about handling sessions from within a client application, see [Gestion de Session MAPI](mapi-session-handling.md)
  
## <a name="see-also"></a>Voir aussi

- [MAPILogonEx](mapilogonex.md)  
- [IMAPISession : IUnknown](imapisessioniunknown.md)
- [Gestion de Session MAPI](mapi-session-handling.md)  
- [Vue d'ensemble de la programmation MAPI](mapi-programming-overview.md)

