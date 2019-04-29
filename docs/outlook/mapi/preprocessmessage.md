---
title: PreprocessMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PreprocessMessage
api_type:
- COM
ms.assetid: dda50325-74b3-445e-986e-115f6536561f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a3982520cb1c745874a938962ece075a294b6257
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437244"
---
# <a name="preprocessmessage"></a>PreprocessMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction qui prétraite le contenu des messages ou le format d'un message.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi. h  <br/> |
|Fonction définie implémentée par:  <br/> |Fournisseurs de transport  <br/> |
|Fonction définie appelée par:  <br/> |Spouleur MAPI  <br/> |
   
```cpp
HRESULT PreprocessMessage(
  LPVOID lpvSession,
  LPMESSAGE lpMessage,
  LPADRBOOK lpAdrBook,
  LPMAPIFOLDER lpFolder,
  LPALLOCATEBUFFER AllocateBuffer,
  LPALLOCATEMORE AllocateMore,
  LPFREEBUFFER FreeBuffer,
  ULONG FAR * lpcOutbound,
  LPMESSAGE FAR * FAR * lpppMessage,
  LPADRLIST FAR * lppRecipList
);
```

## <a name="parameters"></a>Paramètres

 _lpvSession_
  
> dans Pointeur vers la session à utiliser. 
    
 _lpMessage_
  
> dans Pointeur vers le message à prétraiter. 
    
 _lpAdrBook_
  
> dans Pointeur vers le carnet d'adresses à partir duquel l'utilisateur doit sélectionner des destinataires pour le message. 
    
 _lpFolder_
  
> [in, out] Pointeur vers un dossier. Lors de l'entrée, le paramètre _lpFolder_ pointe vers le dossier qui contient les messages à prétraiter. Lors de la sortie, _lpFolder_ pointe vers le dossier où les messages prétraités ont été placés. 
    
 _lpAllocateBuffer_
  
> dans Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire. 
    
 _lpAllocateMore_
  
> dans Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire lorsque cela est nécessaire. 
    
 _lpFreeBuffer_
  
> dans Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) à utiliser pour libérer de la mémoire. 
    
 _lpcOutbound_
  
> remarquer Pointeur vers le nombre de messages dans le tableau vers lequel pointe le paramètre _lpppMessage_ . 
    
 _lpppMessage_
  
> remarquer Pointeur vers un pointeur vers un tableau de pointeurs vers des messages prétraités ou générés. 
    
 _lppRecipList_
  
> remarquer Pointeur vers une structure [ADRLIST](adrlist.md) renvoyée facultative, répertoriant les destinataires détectés par le préprocesseur pour lesquels le message ne peut pas être remis. Pour plus d'informations sur le contenu de cette liste, voir la méthode [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Le contenu du message a été prétraité avec succès.
    
## <a name="remarks"></a>Remarques

Un préprocesseur de message de fournisseur de transport peut présenter un indicateur de progression pendant le prétraitement des messages. Toutefois, il ne doit jamais présenter une boîte de dialogue demandant l'interaction de l'utilisateur pendant le prétraitement des messages. 
  
Lorsqu'un préprocesseur ajoute de grandes quantités de données à un message sortant, certaines procédures doivent être suivies. Ce type de message peut être stocké dans une banque de messages basée sur un serveur, ce qui oblige le préprocesseur à accéder à un magasin distant, une procédure qui prend du temps. Pour éviter cela, le préprocesseur doit disposer d'une option permettant de stocker des données qui occupent beaucoup d'espace dans une banque de messages locale et de fournir une référence à cette banque locale dans le message. 
  
Le préprocesseur ne doit pas libérer les objets transmis à l'origine à la fonction **PreprocessMessage** . 
  
Avant que le spouleur MAPI puisse appeler une fonction **PreprocessMessage** , le fournisseur de transport doit avoir inscrit la fonction dans un appel à la méthode [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) . Après l'appel d'une fonction **PreprocessMessage** , le spouleur ne peut pas continuer à envoyer un message tant que la fonction n'est pas renvoyée. 
  
Le spouleur MAPI est propriétaire de la tâche d'envoi de messages. Cela signifie que le message d'origine n'est jamais placé dans un tableau de pointeurs de message et qu'un appel aux méthodes **SubmitMessage** n'est jamais requis. 
  
## <a name="see-also"></a>Voir aussi



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

