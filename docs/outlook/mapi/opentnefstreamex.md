---
title: OpenTnefStreamEx
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 86905839e65fca85ecdf782a8237335bd933e91c
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62770695"
---
# <a name="opentnefstreamex"></a>OpenTnefStreamEx

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un objet Transport-Neutral Encapsulation Format (TNEF) qui peut être utilisé pour encoder ou décoder un objet message dans un flux de données TNEF à utiliser par les transports, les passerelles et les magasins de messages. Il s’agit du point d’entrée pour l’accès au TNEF. 
  
|||
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
  
> [in] Transmet un objet de support ou transmet NULL. Si la valeur est NULL,  _le paramètre lpAddressBook_ doit être non null. 
    
_lpStream_
  
> [in] Pointeur vers un objet de flux de stockage, tel qu’une interface OLE **IStream** , fournissant une source ou une destination pour un message de flux TNEF. 
    
_lpszStreamName_
  
> [in] Pointeur vers le nom du flux de données utilisé par l’objet TNEF. Si l’appelant a définie l’indicateur TNEF_ENCODE (paramètre _ulFlags_ ) dans son appel à **OpenTnefStream**, le paramètre  _lpszName_ doit spécifier un pointeur non null vers une chaîne non null constituée de tous les caractères considérés comme valides pour nommer un fichier. MAPI n’autorise pas les noms de chaînes, y compris les caractères « [ », « ] » ou « : », même si le système de fichiers autorise leur utilisation. La taille de la chaîne transmise pour le paramètre  _lpszName_ ne doit pas dépasser la valeur de MAX_PATH, la longueur maximale d’une chaîne qui contient un nom de chemin d’accès. 
    
_ulFlags_
  
> [in] Masque de bits d’indicateurs utilisés pour indiquer le mode de la fonction. Les indicateurs suivants peuvent être définies :
    
TNEF_BEST_DATA 
  
> Toutes les propriétés possibles sont mappées dans leurs attributs de bas niveau, mais lorsqu’il existe une perte de données possible en raison de la conversion en attribut de bas niveau, la propriété est également codée dans les encapsulations. Notez que cela entraîne la duplication des informations dans le flux TNEF. TNEF_BEST_DATA est la valeur par défaut si aucun autre mode n’est spécifié. 
    
TNEF_COMPATIBILITY 
  
> Fournit une compatibilité ascendante avec des applications clientes plus anciennes. Les flux TNEF codés avec cet indicateur map fourniront toutes les propriétés possibles dans leur attribut de bas niveau correspondant. Ce mode entraîne également la valeur par défaut de certaines propriétés qui sont requises par les clients de bas niveau. 
    
  > [!CAUTION]
  > Cet indicateur est obsolète et ne doit pas être utilisé. 
  
TNEF_DECODE 
  
> L’objet TNEF sur le flux indiqué est ouvert avec un accès en lecture seule. Le fournisseur de transport doit définir cet indicateur si la fonction doit initialiser l’objet pour un décodage ultérieur.
    
TNEF_ENCODE 
  
> L’objet TNEF sur le flux indiqué est ouvert pour une autorisation de lecture/écriture. Le fournisseur de transport doit définir cet indicateur si la fonction doit initialiser l’objet pour un codage ultérieur.
    
TNEF_PURE 
  
> Encode toutes les propriétés dans les blocs d’encapsulation MAPI. Par conséquent, un fichier TNEF « pur » se compose au maximum des attributs attMAPIProps, attAttachment, attRenddata et attRecipTable. Ce mode est idéal pour une utilisation lorsqu’aucune compatibilité ascendante n’est requise.
    
_lpMessage_
  
> [in] Pointeur vers un objet de message comme destination pour un message décodé avec des pièces jointes ou une source pour un message codé avec des pièces jointes. Toutes les propriétés d’un message de destination peuvent être écrasées par les propriétés d’un message codé.
    
_wKeyVal_
  
> [in] Clé de recherche que l’objet TNEF utilise pour faire correspondre les pièces jointes aux balises de texte insérées dans le texte du message. Cette valeur doit être relativement unique pour tous les messages. 
    
_lpAddressBook_
  
> [in] Pointeur vers un objet de carnet d’adresses utilisé pour obtenir des informations d’adressare pour les identificateurs d’entrée. 
    
_lppTNEF_
  
> [out] Pointeur vers le nouvel objet TNEF.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

La **fonction OpenTnefStreamEx** est le remplacement recommandé [d’OpenTnefStream](opentnefstream.md), le point d’entrée d’origine pour l’accès TNEF. 
  
Un objet TNEF créé par la fonction **OpenTnefStreamEx** appelle ultérieurement la méthode OLE **IUnknown::AddRef** pour ajouter des références pour l’objet de support, l’objet de flux et l’objet message. Le fournisseur de transport peut libérer les références pour les trois objets avec un seul appel à la méthode OLE **IUnknown::Release** sur l’objet TNEF. 
  
**OpenTnefStreamEx** alloue et initialise un objet TNEF pour le fournisseur à utiliser dans le codage d’un message MAPI dans un message de flux TNEF. Sinon, cette fonction peut configurer l’objet que le fournisseur utilisera dans les appels ultérieurs à [ITnef::ExtractProps](itnef-extractprops.md) pour décoder un message de flux TNEF dans un message MAPI. Pour libérer l’objet TNEF et fermer la session, le fournisseur de transport doit appeler la méthode **IUnknown::Release** héritée sur l’objet. 
  
La valeur de base du  _paramètre wKeyVal_ ne doit pas être zéro et ne doit pas être la même pour chaque appel à **OpenTnefStreamEx**. Au lieu de cela, utilisez des nombres aléatoires basés sur l’heure système à partir du générateur de numéros aléatoires de la bibliothèque d’utilisation.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromTNEF  <br/> |MFCMAPI utilise la **méthode OpenTnefStreamEx** pour ouvrir un flux sur le fichier TNEF afin que les propriétés soient extraites. |
   
## <a name="see-also"></a>Voir aussi

- [IMAPISupport : IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

