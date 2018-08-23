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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 878c3aaf22a6cf8a08c8234df41b671088c435c7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584988"
---
# <a name="preprocessmessage"></a>PreprocessMessage

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Définit une fonction qui pré-traite les contenus du message ou le format d’un message.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Fonction implémentée par :  <br/> |Fournisseurs de transport  <br/> |
|Fonction appelée par :  <br/> |Spouleur MAPI  <br/> |
   
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
  
> [in] Pointeur vers le message prétraitement. 
    
 _lpAdrBook_
  
> [in] Pointeur vers le carnet d’adresses à partir de laquelle l’utilisateur doit sélectionner les destinataires du message. 
    
 _lpFolder_
  
> [entrée, sortie] Pointeur vers un dossier. À l’entrée, le paramètre _lpFolder_ pointe vers le dossier qui contient les messages prétraitement. Dans la sortie, _lpFolder_ pointe vers le dossier où les messages prétraités ont été placés. 
    
 _lpAllocateBuffer_
  
> [in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire. 
    
 _lpAllocateMore_
  
> [in] Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) , à utiliser pour allouer de la mémoire supplémentaire si nécessaire. 
    
 _lpFreeBuffer_
  
> [in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire. 
    
 _lpcOutbound_
  
> [out] Pointeur vers le nombre de messages dans le tableau indiqué par le paramètre _lpppMessage_ . 
    
 _lpppMessage_
  
> [out] Pointeur vers un pointeur vers un tableau de pointeurs vers prétraités ou les messages générés dans le cas contraire. 
    
 _lppRecipList_
  
> [out] Pointeur vers une structure [ADRLIST](adrlist.md) renvoyée facultative, liste des destinataires détecté préprocesseur pour laquelle le message est remis. Pour plus d’informations sur le contenu de cette liste, voir la méthode [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) . 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK
  
> Contenu du message ont été prétraité avec succès.
    
## <a name="remarks"></a>Remarques

Un préprocesseur de message-fournisseur de transport peut représenter un indicateur de progression pendant le prétraitement du message. Toutefois, il ne doit jamais présenter une boîte de dialogue solliciter l’utilisateur pendant le prétraitement du message. 
  
Lorsqu’un préprocesseur ajoute des grandes quantités de données à un message sortant, certaines procédures. Ce type de message peut être stocké dans une banque de messages sur le serveur, et le préprocesseur accéder à un magasin distant, beaucoup de temps. Pour éviter d’avoir à le faire, le préprocesseur doit avoir une option qui lui permet de stocker les données qui accepte une grande quantité d’espace dans une banque de messages locale et pour fournir une référence à cette banque locale dans le message. 
  
Le préprocesseur ne doit pas libérer tous les objets initialement transmis à la fonction **PreprocessMessage** basé. 
  
Avant le spouleur MAPI peut appeler une fonction **PreprocessMessage** , le fournisseur de transport doit avoir enregistré la fonction dans un appel à la méthode [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) . Après avoir appelé une fonction **PreprocessMessage** , le spouleur ne peut pas continuer à envoyer un message jusqu'à ce que la fonction renvoie. 
  
Le spouleur MAPI propriétaire de la tâche de soumission de messages. Cela signifie que le message d’origine n’est jamais placé dans un tableau de pointeurs de message et qu’un appel aux méthodes **SubmitMessage** jamais. 
  
## <a name="see-also"></a>Voir aussi



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

