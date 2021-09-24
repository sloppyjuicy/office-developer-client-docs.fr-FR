---
title: PreprocessMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PreprocessMessage
api_type:
- COM
ms.assetid: dda50325-74b3-445e-986e-115f6536561f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 00d2dce81ecb8db1cd69406136b306acc731cc6c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550203"
---
# <a name="preprocessmessage"></a>PreprocessMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction qui prétraite le contenu du message ou le format d’un message.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Fonction définie implémentée par :  <br/> |Fournisseurs de transport  <br/> |
|Fonction définie appelée par :  <br/> |Pooler MAPI  <br/> |
   
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
  
> [in] Pointeur vers la session à utiliser. 
    
 _lpMessage_
  
> [in] Pointeur vers le message à prétraiter. 
    
 _lpAdrBook_
  
> [in] Pointeur vers le carnet d’adresses à partir duquel l’utilisateur doit sélectionner les destinataires du message. 
    
 _lpFolder_
  
> [in, out] Pointeur vers un dossier. Lors de l’entrée,  _le paramètre lpFolder_ pointe vers le dossier qui contient les messages à prétraiter. En sortie,  _lpFolder_ pointe vers le dossier dans lequel les messages prétraités ont été placés. 
    
 _lpAllocateBuffer_
  
> [in] Pointeur vers la [fonction MAPIAllocateBuffer,](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire. 
    
 _lpAllocateMore_
  
> [in] Pointeur vers la [fonction MAPIAllocateMore,](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire si nécessaire. 
    
 _lpFreeBuffer_
  
> [in] Pointeur vers la [fonction MAPIFreeBuffer,](mapifreebuffer.md) à utiliser pour libérer de la mémoire. 
    
 _lpcOutbound_
  
> [out] Pointeur vers le nombre de messages dans le tableau pointés par le _paramètre lpppMessage._ 
    
 _lpppMessage_
  
> [out] Pointeur vers un pointeur vers un tableau de pointeurs vers des messages prétraités ou générés. 
    
 _lppRecipList_
  
> [out] Pointeur vers une structure [ADRLIST](adrlist.md) renvoyée facultative, répertoriant les destinataires détectés par le préprocesseur pour lesquels le message n’est pas remis. Pour plus d’informations sur le contenu de cette liste, voir la méthode [IMAPISupport::StatusRecips.](imapisupport-statusrecips.md) 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Le contenu du message a été correctement prétraité.
    
## <a name="remarks"></a>Remarques

Un préprocesseur de message de fournisseur de transport peut présenter un indicateur de progression pendant le prétraitment du message. Toutefois, elle ne doit jamais présenter de boîte de dialogue nécessitant une interaction de l’utilisateur pendant le prétraitment du message. 
  
Lorsqu’un préprocesseur ajoute de grandes quantités de données à un message sortant, certaines procédures doivent être suivies. Ce type de message peut être stocké dans une magasin de messages basé sur un serveur, ce qui entraîne l’accès du préprocesseur à une magasin distante, une procédure longue. Pour éviter d’avoir à le faire, le préprocesseur doit disposer d’une option qui lui permet de stocker des données qui occupent une grande quantité d’espace dans un magasin de messages local et de fournir une référence à cette boutique locale dans le message. 
  
Le préprocesseur ne doit libérer aucun des objets transmis à l’origine à la **fonction Basée sur PreprocessMessage.** 
  
Avant que lepooler MAPI puisse appeler une fonction **PreprocessMessage,** le fournisseur de transport doit avoir inscrit la fonction dans un appel à la méthode [IMAPISupport::RegisterPreprocessor.](imapisupport-registerpreprocessor.md) Après avoir appelé **une fonction PreprocessMessage,** lepooler ne peut pas continuer à envoyer un message tant que la fonction n’est pas revenu. 
  
Lepooler MAPI est propriétaire de la tâche d’envoi des messages. Cela signifie que le message d’origine n’est jamais placé dans un tableau de pointeurs de message et qu’un appel aux méthodes **SubmitMessage** n’est jamais requis. 
  
## <a name="see-also"></a>Voir aussi



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

