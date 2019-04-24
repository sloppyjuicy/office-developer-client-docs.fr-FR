---
title: IABContainerCopyEntries
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CopyEntries
api_type:
- COM
ms.assetid: 4e775228-5ceb-4002-9b68-999fb5889b86
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: ddb730ed92db4c8d281e7c8d5d9b18bc44505598
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346395"
---
# <a name="iabcontainercopyentries"></a>IABContainer::CopyEntries

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie une ou plusieurs entrées, généralement les utilisateurs de messagerie ou les listes de distribution.
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpEntries_
  
> dans Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui contient les identificateurs d'entrée des entrées à copier. 
    
 _ulUIParam_
  
> dans Handle de la fenêtre parente des boîtes de dialogue ou des fenêtres que cette méthode affiche. Le paramètre _ulUIParam_ doit être égal à zéro si l'indicateur AB_NO_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpProgress_
  
> dans Pointeur vers un objet de progression qui affiche un indicateur de progression, ou NULL. Si _lpProgress_ a la valeur null, un indicateur de progression doit être affiché à l'aide de l'objet de progression fourni par MAPI via la méthode [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) . Le paramètre _lpProgress_ est ignoré si l'indicateur AB_NO_DIALOG est défini dans _ulFlags_.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'exécution de l'opération de copie. Les indicateurs suivants peuvent être définis:
    
AB_NO_DIALOG 
  
> Supprime l'affichage d'un indicateur de progression. Si cet indicateur n'est pas défini, un indicateur de progression s'affiche.
    
CREATE_CHECK_DUP_LOOSE 
  
> Indique qu'un niveau faible de vérification des entrées en double doit être effectué. L'implémentation de la vérification des entrées en double libre est spécifique au fournisseur. Par exemple, un fournisseur peut définir une correspondance libre comme deux entrées portant le même nom complet.
    
CREATE_CHECK_DUP_STRICT 
  
> Indique qu'un niveau strict de vérification des entrées en double doit être effectué. L'implémentation d'une vérification d'entrée stricte en double est propre au fournisseur. Par exemple, un fournisseur peut définir une correspondance stricte comme deux entrées ayant à la fois le même nom d'affichage et l'même adresse de messagerie.
    
CREATE_REPLACE 
  
> Indique qu'une nouvelle entrée doit remplacer une entrée existante si elle est déterminée que les deux sont des doublons.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'opération de copie a réussi.
    
MAPI_W_PARTIAL_COMPLETION 
  
> L'opération de copie a réussi globalement, mais une ou plusieurs entrées n'ont pas pu être copiées. Lorsque cette valeur est renvoyée, l'appel doit être géré comme réussi. Pour tester cette valeur, utilisez la macro **HR_FAILED** . Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IABContainer:: CopyEntries** copie les entrées à partir du même conteneur ou d'un autre conteneur. Un appel à **CopyEntries** est équivalent à l'exécution des appels suivants pour chaque entrée à copier: 
  
1. La méthode [IABContainer:: CreateEntry](iabcontainer-createentry.md) pour créer la nouvelle entrée. 
    
2. La méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) pour lire les propriétés à partir de l'entrée à copier. 
    
3. La méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) pour écrire les propriétés dans la nouvelle entrée. 
    
4. La méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) de la nouvelle entrée pour effectuer une sauvegarde. 
    
5. La méthode [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) de la nouvelle entrée pour libérer la référence du conteneur. 
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Tous les conteneurs qui prennent en charge la méthode **IABContainer:: CopyEntries** doivent être modifiables. Définissez l'indicateur AB_MODIFIABLE de votre conteneur dans sa propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) pour indiquer qu'il est modifiable. 
  
Vous devez prendre en charge tous les indicateurs; Toutefois, l'interprétation et l'utilisation de ces indicateurs sont propres à l'implémentation, autrement dit, vous pouvez déterminer les sémantiques des indicateurs CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT dans le contexte de votre implémentation. Si vous ne pouvez pas ou ne Déterminez pas si une entrée est un doublon, autorisez toujours la copie de l'entrée. 
  
Si l'indicateur CREATE_REPLACE est défini, copiez toujours l'entrée, même si CREATE_CHECK_DUP_LOOSE ou CREATE_CHECK_DUP_STRICT sont définis et si l'entrée est un doublon. 
  
Si CREATE_REPLACE n'est pas défini et que CREATE_CHECK_DUP_STRICT est défini, vérifiez les doublons. Si une entrée est déterminée comme étant un doublon, ne copiez pas l'entrée. 
  
Vous n'avez pas besoin de prendre en charge CREATE_REPLACE; ne pas prendre en charge CREATE_REPLACE signifie que vous pouvez l'ignorer en toute sécurité et toujours effectuer une copie. 
  
Renvoyer l'avertissement MAPI_W_PARTIAL_COMPLETION uniquement si une entrée non dupliquée ne peut pas être copiée. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Utilisez les indicateurs CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT pour indiquer au fournisseur comment vous souhaitez que le conteneur effectue la vérification des entrées en double. Si une entrée doit être ajoutée, qu'il s'agisse ou non d'un doublon, ne définissez aucun de ces indicateurs ou ne définissez pas l'indicateur CREATE_REPLACE. CREATE_REPLACE indique que vous ne vous souciez pas si une entrée est un doublon; vous souhaitez toujours remplacer l'entrée d'origine. 
  
## <a name="see-also"></a>Voir aussi



[ENTRYLIST](entrylist.md)
  
[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

