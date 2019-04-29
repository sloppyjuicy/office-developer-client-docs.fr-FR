---
title: IMAPIPropGetIDsFromNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetIDsFromNames
api_type:
- COM
ms.assetid: e3f501a4-a8ee-43d7-bd83-c94e7980c398
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 28880b818bc80e31cae0c695d4aac92eb9555cac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433583"
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
  
> dans Nombre de noms de propriétés vers lesquels pointe le paramètre _lppPropNames_ . Si _lppPropNames_ a la valeur null, le paramètre _cPropNames_ doit être égal à 0. 
    
 _lppPropNames_
  
> dans Pointeur vers un tableau de noms de propriétés, ou NULL. Transmission des identificateurs de propriété de tous les noms de propriétés de tous les jeux de propriétés dont l'objet dispose d'informations. Le paramètre _lppPropNames_ ne doit pas être null si l'indicateur MAPI_CREATE est défini dans le paramètre _ulFlags_ . 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui indique comment les identificateurs de propriété doivent être retournés. L'indicateur suivant peut être défini:
    
MAPI_CREATE 
  
> Affecte un identificateur de propriété, s'il n'a pas encore été assigné, à un ou plusieurs des noms inclus dans le tableau de noms de propriétés pointé par _lppPropNames_. Cet indicateur inscrit en interne l'identificateur dans la table de mappage name-to-identifier.
    
 _lppPropTags_
  
> remarquer Pointeur vers un pointeur vers un tableau de balises de propriété qui contient des identificateurs de propriété existants ou nouvellement attribués. Les types de propriétés des balises de propriété dans ce tableau sont définis sur **PT_UNSPECIFIED**.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les identificateurs des noms de propriétés spécifiés ont été correctement renvoyés.
    
MAPI_E_NO_SUPPORT 
  
> L'objet ne prend pas en charge les propriétés nommées.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Mémoire inSuffisante pour récupérer les identificateurs.
    
MAPI_E_TOO_BIG 
  
> L'opération ne peut pas être effectuée, car elle nécessite le renvoi d'un trop grand nombre de balises de propriété.
    
MAPI_W_ERRORS_RETURNED 
  
> L'appel a réussi globalement, mais un ou plusieurs identificateurs de propriété n'ont pas pu être renvoyés. Le type de propriété correspondant à chaque propriété indisponible est défini sur **PT_ERROR** et son identificateur sur zéro. Lorsque cet avertissement est renvoyé, gérez l'appel comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp:: GetIDsFromNames** extrait un tableau de balises de propriété qui contiennent les identificateurs de propriété pour une ou plusieurs propriétés nommées. **IMAPIProp:: GetIDsFromNames** peut être appelé pour effectuer les opérations suivantes: 
  
- Créez des identificateurs pour les nouveaux noms.
    
- Récupérez des identificateurs pour des noms spécifiques.
    
- Récupérez les identificateurs de toutes les propriétés nommées incluses dans le mappage de l'objet.
    
Les propriétés nommées sont généralement utilisées par les fournisseurs de banques de messages pour les dossiers et les messages. D'autres objets, tels que les utilisateurs de messagerie et les sections de profil, peuvent ne pas prendre en charge l'Association de noms à des identificateurs de propriétés et renvoyer MAPI_E_NO_SUPPORT à partir de **GetIDsFromNames**.
  
Si une erreur renvoie un identificateur pour un nom particulier, **GetIDsFromNames** renvoie MAPI_W_ERRORS_RETURNED et définit le type de propriété dans l'entrée de tableau de la balise de propriété correspondant au nom de **PT_ERROR** et l'identificateur à zéro. 
  
Le mappage nom-identificateur est représenté par la propriété **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) d'un objet. **PR_MAPPING_SIGNATURE** contient une structure [MAPIUID](mapiuid.md) qui indique le fournisseur de services responsable de l'objet. Si la propriété **PR_MAPPING_SIGNATURE** est identique pour deux objets, partez du principe que ces objets utilisent le même mappage de nom-à-identificateur. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les identificateurs que vous transférez dans le tableau de balises de propriété vers lequel pointe le paramètre _lppPropNames_ doivent être compris dans la plage 0X8000 to 0xFFFE. Les entrées de ce tableau doivent être dans le même ordre que les noms transmis dans le tableau des noms de propriétés pointé par _lppPropNames_. 
  
Si vous prenez en charge les propriétés nommées sur un conteneur, utilisez le même mappage de nom à identificateur pour tous les objets de votre conteneur (autrement dit, n'utilisez pas un mappage différent pour chaque dossier de votre banque de messages ou chaque message de votre dossier).
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Étant donné que les types de propriétés des identificateurs renvoyés dans le tableau de balises de propriété vers lequel pointe _lppPropTags_ sont définis sur **PT_UNSPECIFIED**, vous devrez appeler la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) pour récupérer les types précis. 
  
Si vous déplacez ou copiez des objets avec des propriétés nommées et que les objets source et de destination ont des signatures de mappage différentes comme indiqué par les valeurs de leurs propriétés **PR_MAPPING_SIGNATURE** , vous devez conserver les noms lors de ces opérations. Pour conserver les noms de propriété, ajustez les identificateurs de propriétés correspondants pour qu'ils correspondent au mappage nom-identificateur de l'objet de destination. 
  
Certains objets ont une limite pour le nombre d'identificateurs de propriétés qu'ils peuvent nommer. Si un appel à **GetIDsFromNames** entraîne le dépassement de cette limite, la méthode renvoie MAPI_E_TOO_BIG. Dans ce cas, interrogez l'identificateur. 
  
Pour plus d'informations, consultez la rubrique [MAPI named Properties](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl. cpp  <br/> |CSingleMAPIPropListCtrl:: FindAllNamedPropsUsed  <br/> |MFCMAPI utilise la méthode **IMAPIProp:: GetIDsFromNames** pour obtenir les balises de propriété pour toutes les propriétés nommées qui ont été mappées.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[MAPINAMEID](mapinameid.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[MAPI des propri�t�s nomm�e](mapi-named-properties.md)
  
[Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)

