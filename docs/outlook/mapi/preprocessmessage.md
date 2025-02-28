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
description: Définit une fonction qui prétraite le contenu du message ou le format d’un message pour Outlook 2013 et Outlook 2016.
ms.openlocfilehash: 94a38547eff841f3a9310bdfa51f6501e14b78e0
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64454375"
---
# <a name="preprocessmessage"></a>PreprocessMessage

**S’applique à** : Outlook 2013 | Outlook 2016
  
Définit une fonction qui prétraite le contenu du message ou le format d’un message.
  
|Propriété |Valeur |
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
  
> [in, out] Pointeur vers un dossier. Lors de l’entrée, _le paramètre lpFolder_ pointe vers le dossier qui contient les messages à prétraiter. En sortie, _lpFolder_ pointe vers le dossier dans lequel les messages prétraités ont été placés.

 _lpAllocateBuffer_
  
> [in] Pointeur vers la [fonction MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire.

 _lpAllocateMore_
  
> [in] Pointeur vers la [fonction MAPIAllocateMore](mapiallocatemore.md) , à utiliser pour allouer de la mémoire supplémentaire si nécessaire.

 _lpFreeBuffer_
  
> [in] Pointeur vers la [fonction MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire.

 _lpcOutbound_
  
> [out] Pointeur vers le nombre de messages dans le tableau pointés par _le paramètre lpppMessage_ .

 _lpppMessage_
  
> [out] Pointeur vers un pointeur vers un tableau de pointeurs vers des messages prétraités ou générés.

 _lppRecipList_
  
> [out] Pointeur vers une structure [ADRLIST](adrlist.md) renvoyée facultative, répertoriant les destinataires détectés par le préprocesseur pour lesquels le message n’est pas remis. Pour plus d’informations sur le contenu de cette liste, voir la méthode [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) .

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Le contenu du message a été correctement prétraité.

## <a name="remarks"></a>Remarques

Un préprocesseur de message de fournisseur de transport peut présenter un indicateur de progression pendant le prétraitment du message. Toutefois, elle ne doit jamais présenter de boîte de dialogue nécessitant une interaction de l’utilisateur pendant le prétraitment du message.
  
Lorsqu’un préprocesseur ajoute de grandes quantités de données à un message sortant, certaines procédures doivent être suivies. Ce type de message peut être stocké dans une magasin de messages basé sur un serveur, ce qui entraîne l’accès du préprocesseur à une magasin distante, une procédure longue. Pour éviter d’avoir à le faire, le préprocesseur doit disposer d’une option qui lui permet de stocker des données qui occupent une grande quantité d’espace dans une magasin de messages locale et de fournir une référence à cette boutique locale dans le message.
  
Le préprocesseur ne doit libérer aucun des objets transmis à l’origine à la **fonction basée sur PreprocessMessage** .
  
Avant que lepooler MAPI puisse appeler une fonction **PreprocessMessage** , le fournisseur de transport doit avoir inscrit la fonction dans un appel à la méthode [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) . Après avoir appelé **une fonction PreprocessMessage** , lepooler ne peut pas continuer à envoyer un message tant que la fonction n’est pas revenu.
  
Lepooler MAPI est propriétaire de la tâche d’envoi des messages. Cela signifie que le message d’origine n’est jamais placé dans un tableau de pointeurs de message et qu’un appel aux méthodes **SubmitMessage** n’est jamais requis.
  
## <a name="see-also"></a>Voir aussi

[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)  
[IMAPISupport : IUnknown](imapisupportiunknown.md)
