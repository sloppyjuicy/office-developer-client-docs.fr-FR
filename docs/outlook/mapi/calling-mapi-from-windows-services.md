---
title: Appel de MAPI à partir de services Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f77b3dd9ca8c977574aab337b0df572404061b4a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565864"
---
# <a name="calling-mapi-from-windows-services"></a>Appel de MAPI à partir de services Windows

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Pour activer les applications clientes MAPI qui sont enregistrées en tant que services Windows pour fonctionner avec des fournisseurs de services compatible MAPI, MAPI impose plusieurs limitations et exigences.
  
Clients MAPI ont les limitations suivantes :
  
- Ils ne peuvent pas autoriser une interface utilisateur.
    
- Ils peuvent envoyer des messages uniquement par le biais d’une banque de messages étroitement couplés et de transport fournisseur. En outre, les clients MAPI peuvent envoyer et recevoir des messages à l’aide uniquement le serveur Microsoft Exchange ou un autre fournisseur de transport sur le serveur. En raison de problèmes de sécurité et l’identité entre les applications clientes et le spouleur MAPI, la plupart des fournisseurs de transport ne sont pas pris en charge dans un service. 
    
Toutes les applications clientes MAPI, si elles sont implémentées en tant que services Windows, doivent appeler la fonction [exécuter MAPIInitialize](mapiinitialize.md) pour initialiser les bibliothèques de MAPI. Un appel à la fonction [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) est également nécessaire d’utiliser les bibliothèques OLE. [Exécuter MAPIInitialize](mapiinitialize.md) et [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) émettre des appels à la fonction [CoInitialize](http://msdn.microsoft.com/en-us/library/ms678543%28VS.85%29.aspx) pour initialiser les bibliothèques de composant COM (Object Model). Les clients services doivent définir un indicateur spécial, MAPI_NT_SERVICE, dans le membre **ulFlags** de la structure [MAPIINIT_0](mapiinit_0.md) qui est passé à [exécuter MAPIInitialize](mapiinitialize.md) et dans le paramètre _ulFlags_ qui est transmis à la [MAPILogonEx](mapilogonex.md) fonction pour informer les MAPI de leur implémentation spéciale. 
  
Clients MAPI qui sont écrites en tant que services Windows et écrits avec l’interface client MAPI ont une exigence supplémentaire. Ils doivent définir l’indicateur MAPI_NO_MAIL dans l’appel de [MAPILogonEx](mapilogonex.md). Autres types de clients n’ont pas de définir un indicateur d’ouverture de session, car elle est automatiquement définie par MAPI.
  
Pour gérer les messages dans un thread d’initialisation, un client MAPI qui est implémenté en tant que service effectue les opérations suivantes :
  
1. Appelle la fonction [MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx) lorsque les blocs de thread principal. 
    
2. Appelle la séquence [GetMessage](http://msdn.microsoft.com/en-us/library/ms644936%28VS.85%29.aspx) [TranslateMessage](http://msdn.microsoft.com/en-us/library/ms644955%28VS.85%29.aspx)et à [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934%28VS.85%29.aspx) des fonctions de Windows pour gérer le message lorsque [MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx) renvoie la somme de la valeur du paramètre _nCount_ et valeur de **WAIT_OBJECT_0**, ce qui indique qu’un message est dans la file d’attente.
    
## <a name="see-also"></a>Voir aussi



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[Problèmes d’environnement d’exploitation](operating-environment-issues.md)

