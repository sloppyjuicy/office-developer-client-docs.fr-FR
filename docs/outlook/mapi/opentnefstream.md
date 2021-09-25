---
title: OpenTnefStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.OpenTnefStream
api_type:
- COM
ms.assetid: 912d7799-53ce-42a7-9fbd-f9a6a3a56047
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bcda2b9445fca40ba2f67e25b3d6ae7a949ceb52
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571380"
---
# <a name="opentnefstream"></a>OpenTnefStream

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Appelé par un fournisseur de transport pour lancer une session TNEF (Transport Neutral Encapsulation Format) MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Tnef.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de transport  <br/> |
   
```cpp
HRESULT OpenTnefStream(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName, 
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKey,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a>Paramètres

_lpvSupport_
  
> [in] Transmet un objet de support ou transmet NULL. 
    
_lpStream_
  
> [in] Pointeur vers une interface OLE **IStream** d’objet de flux de stockage fournissant une source ou une destination pour un message de flux TNEF. 
    
_lpszStreamName_
  
> [in] Pointeur vers le nom du flux de données utilisé par l’objet TNEF. Si l’appelant a définie l’indicateur TNEF_ENCODE (paramètre _ulFlags)_ dans son appel à **OpenTnefStream,** le paramètre  _lpszName_ doit spécifier un pointeur non null vers une chaîne non null constituée de tous les caractères considérés comme valides pour nommer un fichier. MAPI n’autorise pas les noms de chaînes, y compris les caractères « [ », « ] » ou « : », même si le système de fichiers autorise leur utilisation. La taille de la chaîne transmise pour  _lpszName_ ne doit pas dépasser la valeur de MAX_PATH, la longueur maximale d’une chaîne qui contient un nom de chemin d’accès. 
    
_ulFlags_
  
> [in] Masque de bits d’indicateurs utilisés pour indiquer le mode de la fonction. Les indicateurs suivants peuvent être définies :
    
TNEF_BEST_DATA 
  
> Toutes les propriétés possibles sont mappées dans leurs attributs de bas niveau, mais lorsqu’il existe une perte de données possible en raison de la conversion en attribut de bas niveau, la propriété est également codée dans les encapsulations. Notez que cela entraîne la duplication des informations dans le flux TNEF. TNEF_BEST_DATA est la valeur par défaut si aucun autre mode n’est spécifié. 
    
TNEF_COMPATIBILITY 
  
> Fournit une compatibilité ascendante avec les anciennes applications clientes. Les flux TNEF codés avec cet indicateur maient toutes les propriétés possibles dans leur attribut de bas niveau correspondant. Ce mode entraîne également la mise en valeur par défaut de certaines propriétés qui sont requises par les clients de bas niveau. 
    
  > [!CAUTION]
  > Cet indicateur est obsolète et ne doit pas être utilisé. 
  
TNEF_DECODE 
  
> L’objet TNEF sur le flux indiqué est ouvert avec un accès en lecture seule. Le fournisseur de transport doit définir cet indicateur s’il souhaite que la fonction initialise l’objet pour un décodage ultérieur.
    
TNEF_ENCODE 
  
> L’objet TNEF sur le flux indiqué est ouvert pour une autorisation de lecture/écriture. Le fournisseur de transport doit définir cet indicateur s’il souhaite que la fonction initialise l’objet pour un codage ultérieur.
    
TNEF_PURE 
  
> Encode toutes les propriétés dans les blocs d’encapsulation MAPI. Par conséquent, un fichier TNEF « pur » se compose au maximum d’attMAPIProps, attAttachment, attRenddata et attRecipTable. Ce mode est idéal pour une utilisation lorsqu’aucune compatibilité ascendante n’est requise.
    
_lpMessage_
  
> [in] Pointeur vers un objet de message comme destination pour un message décodé avec des pièces jointes ou une source pour un message codé avec des pièces jointes. Toutes les propriétés d’un message de destination peuvent être écrasées par les propriétés d’un message codé.
    
_wKey_
  
> [in] Clé de recherche que l’objet TNEF utilise pour faire correspondre les pièces jointes aux balises de texte insérées dans le texte du message. Cette valeur doit être relativement unique pour tous les messages.
    
_lppTNEF_
  
> [out] Pointeur vers le nouvel objet TNEF.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Un objet TNEF créé par la fonction **OpenTnefStream** appelle ultérieurement la méthode OLE **IUnknown::AddRef** pour ajouter des références pour l’objet de support, l’objet de flux et l’objet message. Le fournisseur de transport peut libérer les références pour les trois objets avec un seul appel à la méthode OLE **IUnknown::Release** sur l’objet TNEF. 
  
**OpenTnefStream** alloue et initialise une interface **ITnef** d’objet TNEF pour le fournisseur à utiliser dans le codage d’une interface **IMessage** de message MAPI dans un message de flux TNEF. Sinon, la fonction peut configurer l’objet que le fournisseur utilisera dans les appels ultérieurs à [ITnef::ExtractProps](itnef-extractprops.md) pour décoder un message de flux TNEF dans un message MAPI. Pour libérer l’objet TNEF et fermer la session, le fournisseur de transport doit appeler la méthode **IUnknown::Release** héritée sur l’objet. 
  
Cette fonction est le point d’entrée d’origine pour l’accès TNEF et a été remplacée par [OpenTnefStreamEx,](opentnefstreamex.md) mais elle est toujours utilisée pour la compatibilité pour les utilisateurs qui utilisent déjà le TNEF. 
  
## <a name="see-also"></a>Voir aussi

- [IMAPISupport : IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)

