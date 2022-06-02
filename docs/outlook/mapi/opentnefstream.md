---
title: OpenTnefStream
description: OpenTnefStream appelé par un fournisseur de transport pour lancer une session TNEF (Transport Neutral Encapsulation Format) MAPI.
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
ms.openlocfilehash: b1bc9d4e1feeaf444e049a247c3f94e1a7ec59ea
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65854069"
---
# <a name="opentnefstream"></a>OpenTnefStream

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Appelé par un fournisseur de transport pour lancer une session TNEF (Transport Neutral Encapsulation Format) MAPI. 
  
|Propriété|Valeur|
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
  
> [in] Passe un objet de support ou passe null. 
    
_lpStream_
  
> [in] Pointeur vers une interface OLE **IStream** d’objet de flux de stockage fournissant une source ou une destination pour un message de flux TNEF. 
    
_lpszStreamName_
  
> [in] Pointeur vers le nom du flux de données utilisé par l’objet TNEF. Si l’appelant a défini l’indicateur de TNEF_ENCODE (paramètre _ulFlags_ ) dans son appel à **OpenTnefStream**, le paramètre  _lpszName_ doit spécifier un pointeur non null vers une chaîne non Null composée de caractères considérés comme valides pour nommer un fichier. MAPI n’autorise pas les noms de chaînes, y compris les caractères « [ », « ] » ou « : », même si le système de fichiers autorise leur utilisation. La taille de la chaîne passée pour  _lpszName_ ne doit pas dépasser la valeur de MAX_PATH, la longueur maximale d’une chaîne qui contient un nom de chemin d’accès. 
    
_ulFlags_
  
> [in] Masque de bits des indicateurs utilisés pour indiquer le mode de la fonction. Les indicateurs suivants peuvent être définis :
    
TNEF_BEST_DATA 
  
> Toutes les propriétés possibles sont mappées dans leurs attributs de bas niveau, mais en cas de perte de données possible en raison de la conversion en attribut de bas niveau, la propriété est également encodée dans les encapsulations. Notez que cela entraîne la duplication des informations dans le flux TNEF. TNEF_BEST_DATA est la valeur par défaut si aucun autre mode n’est spécifié. 
    
TNEF_COMPATIBILITY 
  
> Fournit une compatibilité descendante avec les anciennes applications clientes. Les flux TNEF encodés avec cet indicateur mappent toutes les propriétés possibles dans leur attribut de bas niveau correspondant. Ce mode entraîne également la mise par défaut de certaines propriétés requises par les clients de bas niveau. 
    
  > [!CAUTION]
  > Cet indicateur est obsolète et ne doit pas être utilisé. 
  
TNEF_DECODE 
  
> L’objet TNEF sur le flux indiqué est ouvert avec un accès en lecture seule. Le fournisseur de transport doit définir cet indicateur s’il souhaite que la fonction initialise l’objet pour le décodage suivant.
    
TNEF_ENCODE 
  
> L’objet TNEF sur le flux indiqué est ouvert pour l’autorisation de lecture/écriture. Le fournisseur de transport doit définir cet indicateur s’il souhaite que la fonction initialise l’objet pour l’encodage suivant.
    
TNEF_PURE 
  
> Encode toutes les propriétés dans les blocs d’encapsulation MAPI. Par conséquent, un fichier TNEF « pur » se compose, au maximum, d’attMAPIProps, d’attAttachment, d’attRenddata et d’attRecipTable. Ce mode est idéal pour une utilisation quand aucune compatibilité descendante n’est requise.
    
_lpMessage_
  
> [in] Pointeur vers un objet de message en tant que destination pour un message décodé avec des pièces jointes ou une source pour un message encodé avec des pièces jointes. Toutes les propriétés d’un message de destination peuvent être remplacées par les propriétés d’un message encodé.
    
_wKey_
  
> [in] Clé de recherche utilisée par l’objet TNEF pour faire correspondre les pièces jointes aux balises de texte insérées dans le texte du message. Cette valeur doit être relativement unique entre les messages.
    
_lppTNEF_
  
> [out] Pointeur vers le nouvel objet TNEF.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Un objet TNEF créé par la fonction **OpenTnefStream** appelle ultérieurement la méthode OLE **IUnknown::AddRef** pour ajouter des références pour l’objet de support, l’objet stream et l’objet message. Le fournisseur de transport peut libérer les références pour les trois objets avec un seul appel à la méthode OLE **IUnknown::Release** sur l’objet TNEF. 
  
**OpenTnefStream** alloue et initialise une interface **ITnef** d’objet TNEF que le fournisseur doit utiliser pour encoder une interface **IMessage** de message MAPI dans un message de flux TNEF. Sinon, la fonction peut configurer l’objet que le fournisseur doit utiliser dans les appels suivants à [ITnef::ExtractProps](itnef-extractprops.md) pour décoder un message de flux TNEF dans un message MAPI. Pour libérer l’objet TNEF et fermer la session, le fournisseur de transport doit appeler la méthode **IUnknown::Release** héritée sur l’objet. 
  
Cette fonction est le point d’entrée d’origine pour l’accès TNEF et a été remplacée par [OpenTnefStreamEx](opentnefstreamex.md) , mais elle est toujours utilisée pour la compatibilité pour ceux qui utilisent déjà TNEF. 
  
## <a name="see-also"></a>Voir aussi

- [IMAPISupport : IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)

