---
title: IMAPIPropGetIDsFromNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.GetIDsFromNames
api_type:
- COM
ms.assetid: e3f501a4-a8ee-43d7-bd83-c94e7980c398
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4f79e82c1ecbca9f006d60a2eb724fc5900a5d68
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564140"
---
# <a name="imapipropgetidsfromnames"></a>IMAPIProp::GetIDsFromNames

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit les identificateurs de propriété qui correspondent à un ou plusieurs noms de propriété.
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a>Paramètres

 _cPropNames_
  
> [in] Nombre de noms de propriétés pointés par _le paramètre lppPropNames._ Si  _lppPropNames est_ NULL, le paramètre  _cPropNames_ doit être 0. 
    
 _lppPropNames_
  
> [in] Pointeur vers un tableau de noms de propriétés, ou NULL. La transmission de NULL demande des identificateurs de propriété pour tous les noms de propriété dans tous les jeux de propriétés sur lesquels l’objet possède des informations. Le _paramètre lppPropNames_ ne doit pas être NULL si l’MAPI_CREATE est définie dans _le paramètre ulFlags._ 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui indique comment les identificateurs de propriété doivent être renvoyés. L’indicateur suivant peut être définie :
    
MAPI_CREATE 
  
> Affecte un identificateur de propriété, s’il n’en a pas encore été affecté, à un ou plusieurs des noms inclus dans le tableau des noms de propriétés pointés par  _lppPropNames_. Cet indicateur inscrit en interne l’identificateur dans la table de mappage nom à identificateur.
    
 _lppPropTags_
  
> [out] Pointeur vers un pointeur vers un tableau de balises de propriété qui contient des identificateurs de propriétés existants ou nouvellement attribués. Les types de propriété pour les balises de propriété dans ce tableau sont PT_UNSPECIFIED **.**
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les identificateurs des noms de propriété spécifiés ont été renvoyés avec succès.
    
MAPI_E_NO_SUPPORT 
  
> L’objet ne prend pas en charge les propriétés nommées.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Une mémoire insuffisante était disponible pour récupérer les identificateurs.
    
MAPI_E_TOO_BIG 
  
> L’opération ne peut pas être effectuée, car elle nécessite un trop grand nombre de balises de propriété à retourner.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi globalement, mais un ou plusieurs identificateurs de propriété n’ont pas pu être renvoyés. Le type de propriété correspondant pour chaque propriété indisponible est PT_ERROR **et** son identificateur sur zéro. Lorsque cet avertissement est renvoyé, traitez l’appel comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED.** Voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIProp::GetIDsFromNames** récupère un tableau de balises de propriétés qui détiennent les identificateurs de propriété pour une ou plusieurs propriétés nommées. **IMAPIProp::GetIDsFromNames** peut être appelé pour : 
  
- Créez des identificateurs pour les nouveaux noms.
    
- Récupérer des identificateurs pour des noms spécifiques.
    
- Récupérez les identificateurs de toutes les propriétés nommées incluses dans le mappage de l’objet.
    
Les propriétés nommées sont généralement utilisées par les fournisseurs de magasins de messages pour les dossiers et les messages. D’autres objets, tels que les utilisateurs de messagerie et les sections de profil, peuvent ne pas prendre en charge l’association de noms aux identificateurs de propriété et peuvent renvoyer des MAPI_E_NO_SUPPORT à partir de **GetIDsFromNames**.
  
En cas d’erreur qui renvoie un identificateur pour un nom particulier, **GetIDsFromNames** renvoie MAPI_W_ERRORS_RETURNED et définit le type de propriété dans l’entrée du tableau de balises de propriétés qui correspond au nom à **PT_ERROR** et à l’identificateur sur zéro. 
  
Le mappage de nom à identificateur est représenté par la propriété **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)). **PR_MAPPING_SIGNATURE** contient une structure [MAPIUID](mapiuid.md) qui indique le fournisseur de services responsable de l’objet. Si la **PR_MAPPING_SIGNATURE** est identique pour deux objets, supposons que ces objets utilisent le même mappage nom à identificateur. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les identificateurs que vous passez dans le tableau de balises de propriétés pointant vers le paramètre  _lppPropNames_ doivent se trouver dans la 0x8000 pour 0xFFFE plage. Les entrées de ce tableau doivent être dans le même ordre que les noms transmis dans le tableau de noms de propriétés pointés par  _lppPropNames_. 
  
Si vous utilisez des propriétés nommées sur un conteneur, utilisez le même mappage nom à identificateur pour tous les objets de votre conteneur (c’est-à-dire, n’utilisez pas de mappage différent pour chaque dossier de votre magasin de messages ou chaque message de votre dossier).
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Étant donné que les types de propriétés pour les identificateurs renvoyés dans le tableau de balises de propriétés pointés par  _lppPropTags_ sont définies sur **PT_UNSPECIFIED**, vous devez appeler la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) pour récupérer les types précis. 
  
Si vous déplacez ou copiez des objets avec des propriétés nommées et que les objets source et destination ont des signatures de mappage différentes, comme indiqué par les valeurs de leurs propriétés **PR_MAPPING_SIGNATURE,** vous devez conserver les noms au cours de ces opérations. Pour conserver les noms des propriétés, ajustez les identificateurs de propriété correspondants pour qu’ils correspondent au mappage nom à identificateur de l’objet de destination. 
  
Certains objets ont une limite quant au nombre d’identificateurs de propriété qu’ils peuvent nommer. Si un appel **à GetIDsFromNames** dépasse cette limite, la méthode renvoie MAPI_E_TOO_BIG. Dans ce cas, interrogez par identificateur. 
  
Pour plus d’informations, voir [PROPRIÉTÉS nommées MAPI.](mapi-named-properties.md) 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedPropsUsed  <br/> |MFCMAPI utilise la méthode **IMAPIProp::GetIDsFromNames** pour obtenir des balises de propriété pour toutes les propriétés nommées qui ont été mappées.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[MAPINAMEID](mapinameid.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[MAPI des propri�t�s nomm�e](mapi-named-properties.md)
  
[Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)

