---
title: OpenTnefStreamEx
description: OpenTnefStreamEx crée un objet TNEF qui peut être utilisé pour encoder ou décoder un objet de message dans un flux de données TNEF.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.OpenTnefStreamEx
api_type:
- COM
ms.assetid: eb84c408-2d8b-453b-92f4-5fd8851b84ca
ms.openlocfilehash: c903e52c4d21c951005422b1e0964d3c0f29a0e2
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65854076"
---
# <a name="opentnefstreamex"></a>OpenTnefStreamEx

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un objet Transport-Neutral Encapsulation Format (TNEF) qui peut être utilisé pour encoder ou décoder un objet de message dans un flux de données TNEF à utiliser par les transports, passerelles et magasins de messages. Il s’agit du point d’entrée pour l’accès TNEF. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Tnef.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de transport  <br/> |
   
```cpp
HRESULT OpenTnefStreamEx(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName,
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKeyVal,
  LPADDRESSBOOK lpAddressBook,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a>Paramètres

_lpvSupport_
  
> [in] Passe un objet de support ou passe null. Si la valeur est NULL, le paramètre  _lpAddressBook_ doit être non null. 
    
_lpStream_
  
> [in] Pointeur vers un objet de flux de stockage, tel qu’une interface OLE **IStream** , fournissant une source ou une destination pour un message de flux TNEF. 
    
_lpszStreamName_
  
> [in] Pointeur vers le nom du flux de données utilisé par l’objet TNEF. Si l’appelant a défini l’indicateur de TNEF_ENCODE (paramètre _ulFlags_ ) dans son appel à **OpenTnefStream**, le paramètre  _lpszName_ doit spécifier un pointeur non null vers une chaîne non Null composée de caractères considérés comme valides pour nommer un fichier. MAPI n’autorise pas les noms de chaînes, y compris les caractères « [ », « ] » ou « : », même si le système de fichiers autorise leur utilisation. La taille de la chaîne passée pour le paramètre  _lpszName_ ne doit pas dépasser la valeur de MAX_PATH, la longueur maximale d’une chaîne qui contient un nom de chemin d’accès. 
    
_ulFlags_
  
> [in] Masque de bits des indicateurs utilisés pour indiquer le mode de la fonction. Les indicateurs suivants peuvent être définis :
    
TNEF_BEST_DATA 
  
> Toutes les propriétés possibles sont mappées dans leurs attributs de bas niveau, mais en cas de perte de données possible en raison de la conversion en attribut de bas niveau, la propriété est également encodée dans les encapsulations. Notez que cela entraîne la duplication des informations dans le flux TNEF. TNEF_BEST_DATA est la valeur par défaut si aucun autre mode n’est spécifié. 
    
TNEF_COMPATIBILITY 
  
> Fournit une compatibilité descendante avec les applications clientes plus anciennes. Les flux TNEF encodés avec cet indicateur mappent toutes les propriétés possibles dans leur attribut de bas niveau correspondant. Ce mode entraîne également la mise par défaut de certaines propriétés requises par les clients de bas niveau. 
    
  > [!CAUTION]
  > Cet indicateur est obsolète et ne doit pas être utilisé. 
  
TNEF_DECODE 
  
> L’objet TNEF sur le flux indiqué est ouvert avec un accès en lecture seule. Le fournisseur de transport doit définir cet indicateur si la fonction est d’initialiser l’objet pour le décodage suivant.
    
TNEF_ENCODE 
  
> L’objet TNEF sur le flux indiqué est ouvert pour l’autorisation de lecture/écriture. Le fournisseur de transport doit définir cet indicateur si la fonction est d’initialiser l’objet pour l’encodage suivant.
    
TNEF_PURE 
  
> Encode toutes les propriétés dans les blocs d’encapsulation MAPI. Par conséquent, un fichier TNEF « pur » se compose, au plus, des attributs attMAPIProps, attAttachment, attRenddata et attRecipTable. Ce mode est idéal pour une utilisation quand aucune compatibilité descendante n’est requise.
    
_lpMessage_
  
> [in] Pointeur vers un objet de message en tant que destination pour un message décodé avec des pièces jointes ou une source pour un message encodé avec des pièces jointes. Toutes les propriétés d’un message de destination peuvent être remplacées par les propriétés d’un message encodé.
    
_wKeyVal_
  
> [in] Clé de recherche utilisée par l’objet TNEF pour faire correspondre les pièces jointes aux balises de texte insérées dans le texte du message. Cette valeur doit être relativement unique entre les messages. 
    
_lpAddressBook_
  
> [in] Pointeur vers un objet carnet d’adresses utilisé pour obtenir des informations d’adressage pour les identificateurs d’entrée. 
    
_lppTNEF_
  
> [out] Pointeur vers le nouvel objet TNEF.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

La fonction **OpenTnefStreamEx** est le remplacement recommandé pour [OpenTnefStream](opentnefstream.md), le point d’entrée d’origine pour l’accès TNEF. 
  
Un objet TNEF créé par la fonction **OpenTnefStreamEx** appelle ultérieurement la méthode OLE **IUnknown::AddRef** pour ajouter des références pour l’objet de support, l’objet stream et l’objet message. Le fournisseur de transport peut libérer les références pour les trois objets avec un seul appel à la méthode OLE **IUnknown::Release** sur l’objet TNEF. 
  
**OpenTnefStreamEx** alloue et initialise un objet TNEF que le fournisseur doit utiliser pour encoder un message MAPI dans un message de flux TNEF. Cette fonction peut également configurer l’objet que le fournisseur doit utiliser dans les appels suivants à [ITnef::ExtractProps](itnef-extractprops.md) pour décoder un message de flux TNEF dans un message MAPI. Pour libérer l’objet TNEF et fermer la session, le fournisseur de transport doit appeler la méthode **IUnknown::Release** héritée sur l’objet. 
  
La valeur de base du paramètre  _wKeyVal_ ne doit pas être égale à zéro et ne doit pas être la même pour chaque appel à **OpenTnefStreamEx**. Utilisez plutôt des nombres aléatoires en fonction de l’heure système du générateur de nombres aléatoires de la bibliothèque runtime.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromTNEF  <br/> |MFCMAPI utilise la méthode **OpenTnefStreamEx** pour ouvrir un flux sur le fichier TNEF afin que les propriétés puissent être extraites. |
   
## <a name="see-also"></a>Voir aussi

- [IMAPISupport : IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

