---
title: IMAPIPropGetIDsFromNames
description: IMAPIPropGetIDsFromNames fournit les identificateurs de propriété qui correspondent à un ou plusieurs noms de propriétés.
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
ms.openlocfilehash: 0f18b4cc318989b9db3ed0f4a8080c200e157a9b
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817066"
---
# <a name="imapipropgetidsfromnames"></a>IMAPIProp::GetIDsFromNames

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit les identificateurs de propriété qui correspondent à un ou plusieurs noms de propriétés.
  
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
  
> [in] Nombre de noms de propriétés pointés par le paramètre  _lppPropNames_ . Si  _lppPropNames_ a la valeur NULL, le paramètre  _cPropNames_ doit être 0. 
    
 _lppPropNames_
  
> [in] Pointeur vers un tableau de noms de propriétés, ou NULL. Le passage de null demande des identificateurs de propriété pour tous les noms de propriétés dans tous les jeux de propriétés sur lesquels l’objet contient des informations. Le paramètre  _lppPropNames_ ne doit pas être NULL si l’indicateur MAPI_CREATE est défini dans le paramètre _ulFlags_ . 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui indique comment les identificateurs de propriété doivent être retournés. L’indicateur suivant peut être défini :
    
MAPI_CREATE 
  
> Affecte un identificateur de propriété, s’il n’en a pas encore été attribué, à un ou plusieurs des noms inclus dans le tableau de noms de propriétés pointé par  _lppPropNames_. Cet indicateur inscrit en interne l’identificateur dans la table de mappage de nom à identificateur.
    
 _lppPropTags_
  
> [out] Pointeur vers un pointeur vers un tableau de balises de propriété qui contient des identificateurs de propriété existants ou nouvellement affectés. Les types de propriétés pour les balises de propriété dans ce tableau sont définis sur **PT_UNSPECIFIED**.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les identificateurs des noms de propriétés spécifiés ont été retournés avec succès.
    
MAPI_E_NO_SUPPORT 
  
> L’objet ne prend pas en charge les propriétés nommées.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Mémoire insuffisante disponible pour récupérer les identificateurs.
    
MAPI_E_TOO_BIG 
  
> L’opération ne peut pas être effectuée, car elle nécessite trop de balises de propriété pour être retournées.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi dans l’ensemble, mais un ou plusieurs identificateurs de propriété n’ont pas pu être retournés. Le type de propriété correspondant pour chaque propriété indisponible est défini sur **PT_ERROR** et son identificateur sur zéro. Lorsque cet avertissement est retourné, gérez l’appel comme ayant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Consultez [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp::GetIDsFromNames** récupère un tableau de balises de propriétés qui contiennent les identificateurs de propriété pour une ou plusieurs propriétés nommées. **IMAPIProp::GetIDsFromNames** peut être appelé pour effectuer les opérations suivantes : 
  
- Créez des identificateurs pour les nouveaux noms.
    
- Récupérez les identificateurs pour des noms spécifiques.
    
- Récupérez les identificateurs de toutes les propriétés nommées incluses dans le mappage de l’objet.
    
Les propriétés nommées sont généralement utilisées par les fournisseurs de magasins de messages pour les dossiers et les messages. D’autres objets, tels que les utilisateurs de messagerie et les sections de profil, peuvent ne pas prendre en charge l’association de noms aux identificateurs de propriété et peuvent retourner MAPI_E_NO_SUPPORT à partir de **GetIDsFromNames**.
  
S’il existe une erreur qui retourne un identificateur pour un nom particulier, **GetIDsFromNames** retourne MAPI_W_ERRORS_RETURNED et définit le type de propriété dans l’entrée de tableau de balises de propriétés qui correspond au nom à **PT_ERROR** et l’identificateur à zéro. 
  
Le mappage de nom à identificateur est représenté par la propriété **PR_MAPPING_SIGNATURE** d’un objet ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)). **PR_MAPPING_SIGNATURE** contient une structure [MAPIUID](mapiuid.md) qui indique le fournisseur de services responsable de l’objet. Si la propriété **PR_MAPPING_SIGNATURE** est la même pour deux objets, supposons que ces objets utilisent le même mappage de nom à identificateur. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les identificateurs que vous transmettez dans le tableau de balises de propriétés pointé par le paramètre  _lppPropNames_ doivent se trouver dans le 0x8000 pour 0xFFFE plage. Les entrées de ce tableau doivent être dans le même ordre que les noms passés dans le tableau de noms de propriétés pointés par  _lppPropNames_. 
  
Si vous prenez en charge les propriétés nommées sur un conteneur, utilisez le même mappage de nom à identificateur pour tous les objets de votre conteneur (autrement dit, n’utilisez pas un mappage différent pour chaque dossier de votre magasin de messages ou chaque message de votre dossier).
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Étant donné que les types de propriétés des identificateurs retournés dans le tableau de balises de propriétés pointés par  _lppPropTags_ sont définis sur **PT_UNSPECIFIED**, vous devez appeler la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) pour récupérer les types précis. 
  
Si vous déplacez ou copiez des objets avec des propriétés nommées et que les objets source et de destination ont des signatures de mappage différentes, comme indiqué par les valeurs de leurs propriétés **PR_MAPPING_SIGNATURE** , vous devez conserver les noms pendant ces opérations. Pour conserver les noms de propriétés, ajustez les identificateurs de propriété correspondants pour qu’ils correspondent au mappage nom-identificateur de l’objet de destination. 
  
Certains objets ont une limite quant au nombre d’identificateurs de propriété qu’ils peuvent nommer. Si un appel à **GetIDsFromNames** entraîne le dépassement de cette limite, la méthode retourne MAPI_E_TOO_BIG. Dans ce cas, interrogez par identificateur. 
  
Pour plus d’informations, consultez [propriétés nommées MAPI](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedPropsUsed  <br/> |MFCMAPI utilise la méthode **IMAPIProp::GetIDsFromNames pour obtenir des balises** de propriété pour toutes les propriétés nommées qui ont été mappées. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[MAPINAMEID](mapinameid.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[MAPI des propri�t�s nomm�e](mapi-named-properties.md)
  
[Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)

