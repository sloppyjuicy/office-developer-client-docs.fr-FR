---
title: OpenTnefStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStreamEx
api_type:
- COM
ms.assetid: eb84c408-2d8b-453b-92f4-5fd8851b84ca
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b651a913855e99e2f26dfd99fb725cc332201932
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565185"
---
# <a name="opentnefstreamex"></a>OpenTnefStreamEx

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Crée un objet de Transport-Neutral Encapsulation Format (TNEF) qui peut servir à coder ou décoder un objet de message dans un flux de données TNEF pour une utilisation par les transports ou des passerelles et des banques de messages. Il s’agit du point d’entrée pour l’accès TNEF. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |TNEF.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de transport  <br/> |
   
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
  
> [in] Transmet un objet de prise en charge, ou passe NULL. Si la valeur NULL, le paramètre _lpAddressBook_ doit être non null. 
    
_lpStream_
  
> [in] Pointeur vers un objet stream de stockage, par exemple une interface OLE **IStream** , fournissant une source ou destination d’un message de flux TNEF. 
    
_lpszStreamName_
  
> [in] Pointeur vers le nom du flux de données qui utilise l’objet TNEF. Si l’appelant a défini l’indicateur TNEF_ENCODE (paramètre _ulFlags_ ) l’appel vers **OpenTnefStream**, le paramètre de _caractère_ doit spécifier un pointeur non null à une chaîne non nulle constituée de caractères validités pour un fichier d’attribution de noms. MAPI n’autorise pas les noms de chaîne, y compris les caractères « [ », «] », ou « : », même si le système de fichiers permet de leur utilisation. La taille de la chaîne transmise au paramètre _le caractère_ ne doit pas dépasser la valeur de MAX_PATH, la longueur maximale d’une chaîne qui contient un nom de chemin d’accès. 
    
_ulFlags_
  
> [in] Masque de bits d’indicateurs utilisés pour indiquer le mode de la fonction. Les indicateurs suivants peuvent être définis :
    
TNEF_BEST_DATA 
  
> Toutes les propriétés possibles sont mappées dans leurs attributs de bas niveau, mais lorsqu’il existe une perte de données possible en raison de la conversion à un attribut de bas niveau, la propriété est également codée dans l’encapsule. Notez que cette opération entraîne la duplication des informations sur le flux TNEF. TNEF_BEST_DATA est la valeur par défaut si aucun autre mode n’est spécifiés. 
    
TNEF_COMPATIBILITY 
  
> Fournit une compatibilité descendante avec les applications clientes antérieures. Flux TNEF codés avec cet indicateur mappe toutes les propriétés possibles dans leur attribut de bas niveau correspondant. Ce mode entraîne également l’utilisation par défaut de certaines propriétés requises par les clients de bas niveau. 
    
  > [!CAUTION]
  > Cet indicateur est obsolète et ne doit pas être utilisé. 
  
TNEF_DECODE 
  
> L’objet TNEF sur le flux indiqué est ouvert avec accès en lecture seule. Le fournisseur de transport doit définir cet indicateur si la fonction est d’initialiser l’objet de décodage suivantes.
    
TNEF_ENCODE 
  
> Ouverture de l’objet TNEF sur le flux indiqué pour l’autorisation en lecture-écriture. Le fournisseur de transport doit définir cet indicateur si la fonction est d’initialiser l’objet de codage suivantes.
    
TNEF_PURE 
  
> Code toutes les propriétés dans les blocs d’encapsulation MAPI. Par conséquent, un fichier TNEF « pur » est constitué, au plus, les attributs attMAPIProps, attAttachment, attRenddata et attRecipTable. Ce mode est idéal pour une utilisation lorsque aucune compatibilité descendante n’est nécessaire.
    
_lpMessage_
  
> [in] Pointeur vers un objet de message comme une destination d’un message décodée avec les pièces jointes ou d’une source d’un message codé avec les pièces jointes. Toutes les propriétés d’un message de destination peuvent être remplacées par les propriétés d’un message codé.
    
_wKeyVal_
  
> [in] Une clé de recherche que l’objet TNEF utilise pour la correspondance de pièces jointes sur les balises de texte insérés dans le texte du message. Cette valeur doit être relativement unique sur les messages. 
    
_lpAddressBook_
  
> [in] Pointeur vers un objet de carnet d’adresses utilisé pour obtenir des informations d’adressage des identificateurs d’entrée. 
    
_lppTNEF_
  
> [out] Pointeur vers le nouvel objet TNEF.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

La fonction **OpenTnefStreamEx** est le remplacement recommandé pour [OpenTnefStream](opentnefstream.md), le point d’entrée d’origine pour l’accès TNEF. 
  
Un objet TNEF créé ultérieurement par la fonction **OpenTnefStreamEx** appelle la méthode OLE **IUnknown::AddRef** pour ajouter des références pour l’objet de prise en charge, l’objet stream et l’objet du message. Le fournisseur de transport permettre libérer les références pour tous les trois objets avec un seul appel à la méthode OLE **IUnknown::Release** sur l’objet TNEF. 
  
**OpenTnefStreamEx** alloue et initialise un objet TNEF pour le fournisseur à utiliser dans le codage d’un message MAPI dans un message de flux TNEF. Cette fonction peut également définir l’objet pour le fournisseur à utiliser dans les appels suivants à [ITnef::ExtractProps](itnef-extractprops.md) pour décoder un message de flux TNEF dans un message MAPI. Pour libérer de l’objet TNEF, fermez la session, le fournisseur de transport doit appeler la méthode **IUnknown::Release** héritée sur l’objet. 
  
La valeur de base pour le paramètre _wKeyVal_ ne doit pas être zéro et ne doit pas être la même pour chaque appel à **OpenTnefStreamEx**. Au lieu de cela, utilisez des nombres aléatoires en fonction de l’heure système à partir du Générateur de nombres aléatoires de la bibliothèque d’exécution.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromTNEF  <br/> |MFCMAPI utilise la méthode **OpenTnefStreamEx** pour ouvrir un flux de données sur le fichier TNEF afin que les propriétés peuvent être extraits.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [IMAPISupport : IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

