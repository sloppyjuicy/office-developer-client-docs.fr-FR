---
title: OpenTnefStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStream
api_type:
- COM
ms.assetid: 912d7799-53ce-42a7-9fbd-f9a6a3a56047
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 524b52026010b9a06d5822b48b7c04bbf90a113e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348922"
---
# <a name="opentnefstream"></a>OpenTnefStream

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Appelé par un fournisseur de transport pour lancer une session TNEF (Transport Neutral Encapsulation Format) MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |TNEF. h  <br/> |
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
  
> dans Transmet un objet support ou transmet une valeur NULL. 
    
_lpStream_
  
> dans Pointeur vers une interface OLE **IStream** d'objet de flux de stockage fournissant une source ou une destination pour un message de flux TNEF. 
    
_lpszStreamName_
  
> dans Pointeur vers le nom du flux de données que l'objet TNEF utilise. Si l'appelant a défini l'indicateur TNEF_ENCODE (paramètre _ulFlags_ ) dans son appel à **OpenTnefStream**, le paramètre _lpszName_ doit spécifier un pointeur non null vers une chaîne non null constituée de tous les caractères considérés comme valides pour l'attribution d'un nom à un fichier. MAPI n'autorise pas les noms de chaînes, y compris les caractères «[», «]» ou «:», même si le système de fichiers autorise leur utilisation. La taille de la chaîne transmise pour _lpszName_ ne doit pas dépasser la valeur de MAX_PATH, la longueur maximale d'une chaîne contenant un nom de chemin d'accès. 
    
_ulFlags_
  
> dans Masque de des indicateurs utilisé pour indiquer le mode de la fonction. Les indicateurs suivants peuvent être définis:
    
TNEF_BEST_DATA 
  
> Toutes les propriétés possibles sont mappées dans leurs attributs de bas niveau, mais en cas de perte de données possible en raison de la conversion en un attribut de bas niveau, la propriété est également codée dans les encapsulations. Notez que cette opération entraînera la duplication des informations dans le flux TNEF. TNEF_BEST_DATA est la valeur par défaut si aucun autre mode n'est spécifié. 
    
TNEF_COMPATIBILITY 
  
> Fournit une compatibilité descendante avec les applications clientes plus anciennes. Les flux TNEF codés avec cet indicateur mappent toutes les propriétés possibles dans leur attribut de bas niveau correspondant. Ce mode provoque également la valeur par défaut de certaines propriétés requises par les clients de bas niveau. 
    
  > [!CAUTION]
  > Cet indicateur est obsolète et ne doit pas être utilisé. 
  
TNEF_DECODE 
  
> L'objet TNEF sur le flux indiqué est ouvert avec un accès en lecture seule. Le fournisseur de transport doit définir cet indicateur s'il souhaite que la fonction initialise l'objet pour un décodage ultérieur.
    
TNEF_ENCODE 
  
> L'objet TNEF sur le flux indiqué est ouvert en lecture/écriture. Le fournisseur de transport doit définir cet indicateur s'il souhaite que la fonction initialise l'objet pour le codage suivant.
    
TNEF_PURE 
  
> Encode toutes les propriétés dans les blocs d'encapsulation MAPI. Par conséquent, un fichier TNEF «pur» se compose au plus des attMAPIProps, attAttachment, attRenddata et attRecipTable. Ce mode est idéal pour une utilisation sans compatibilité descendante.
    
_lpMessage_
  
> dans Pointeur vers un objet message comme destination d'un message décodé avec des pièces jointes ou une source pour un message encodé avec des pièces jointes. Toutes les propriétés d'un message de destination peuvent être remplacées par les propriétés d'un message encodé.
    
_wKey_
  
> dans Clé de recherche utilisée par l'objet TNEF pour faire correspondre les pièces jointes aux balises de texte insérées dans le texte du message. Cette valeur doit être relativement unique dans les messages.
    
_lppTNEF_
  
> remarquer Pointeur vers le nouvel objet TNEF.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Un objet TNEF créé par la fonction **OpenTnefStream** appelle ensuite la méthode OLE **IUnknown:: AddRef** pour ajouter des références pour l'objet de prise en charge, l'objet Stream et l'objet message. Le fournisseur de transport peut libérer les références pour les trois objets avec un seul appel à la méthode OLE **IUnknown:: Release** sur l'objet TNEF. 
  
**OpenTnefStream** alloue et Initialise une interface **ITNEF** d'objets TNEF que le fournisseur doit utiliser pour coder une interface **IMessage** de message MAPI en un message de flux TNEF. La fonction peut également configurer l'objet pour le fournisseur à utiliser dans les appels ultérieurs à [ITnef:: ExtractProps](itnef-extractprops.md) pour décoder un message TNEF en flux TNEF dans un message MAPI. Pour libérer l'objet TNEF et fermer la session, le fournisseur de transport doit appeler la méthode **IUnknown:: Release** héritée sur l'objet. 
  
Cette fonction est le point d'entrée d'origine pour l'accès TNEF et a été remplacée par [OpenTnefStreamEx](opentnefstreamex.md) mais est toujours utilisée pour la compatibilité pour ceux qui utilisent déjà TNEF. 
  
## <a name="see-also"></a>Voir aussi

- [IMAPISupport : IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)

