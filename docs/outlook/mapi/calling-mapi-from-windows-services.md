---
title: Appel de MAPI à partir de Windows Services
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a606b8bf82ce4c06c8e55f6e4df94220bc67501d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318103"
---
# <a name="calling-mapi-from-windows-services"></a>Appel de MAPI à partir de Windows Services

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour permettre aux applications clientes MAPI écrites en tant que services Windows de fonctionner avec des fournisseurs de services conformes MAPI, MAPI impose plusieurs limitations et exigences.
  
Les clients MAPI ont les limitations suivantes :
  
- Ils ne peuvent pas autoriser une interface utilisateur.
    
- Ils peuvent envoyer des messages uniquement par le biais d’un fournisseur de transport et d’une magasin de messages étroitement couplés. En outre, les clients MAPI peuvent envoyer et recevoir des messages en utilisant uniquement le Microsoft Exchange Server ou un autre fournisseur de transport basé sur un serveur. En raison de problèmes d’identité et de sécurité entre les applications clientes et lepooler MAPI, la plupart des fournisseurs de transport ne sont pas pris en charge dans un service. 
    
Toutes les applications clientes MAPI, qu’elles soient implémentées en tant que services Windows, doivent appeler la fonction [MAPIInitialize](mapiinitialize.md) pour initialiser les bibliothèques MAPI. Un appel à la [fonction OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) est également nécessaire pour utiliser les bibliothèques OLE. [MAPIInitialize](mapiinitialize.md) et [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) appellent la fonction [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) pour initialiser les bibliothèques COM (Component Object Model). Les clients qui sont des services doivent définir un indicateur spécial, MAPI_NT_SERVICE, dans le membre **ulFlags** de la structure MAPIINIT_0 qui [est](mapiinit_0.md) transmis à [MAPIInitialize](mapiinitialize.md) et dans le paramètre  _ulFlags_ qui est transmis à la fonction [MAPILogonEx](mapilogonex.md) pour informer MAPI de leur implémentation spéciale. 
  
Les clients MAPI écrits en tant que services Windows et écrits avec l’interface cliente MAPI ont une exigence supplémentaire. Ils doivent définir l’MAPI_NO_MAIL dans l’appel à [MAPILogonEx](mapilogonex.md). Les autres types de clients n’ont pas à définir d’indicateur pour l’accès, car il est automatiquement définie par MAPI.
  
Pour gérer les messages dans un thread d’initialisation, un client MAPI implémenté en tant que service :
  
1. Appelle la [fonction MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) lorsque le thread principal se bloque. 
    
2. Appelle la [séquence getMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx), [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)et [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) des fonctions Windows pour gérer le message lorsque [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) renvoie la somme de la valeur du paramètre  _nCount_ et la valeur de **WAIT_OBJECT_0**, qui indique qu’un message est dans la file d’attente.
    
## <a name="see-also"></a>Voir aussi



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[Problèmes de l’environnement d’exploitation](operating-environment-issues.md)

