---
title: Rôle du fournisseur de carnets d’adresses étranger
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6d532ed4-7dc5-46a9-995a-72bc97d16f6e
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 300681bd585e9d534113404a82f43565f4e79bb4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331207"
---
# <a name="acting-as-a-foreign-address-book-provider"></a>Rôle du fournisseur de carnets d’adresses étranger

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un fournisseur étranger est un fournisseur de carnets d'adresses qui: 
  
- Affecte des identificateurs de modèle à ses destinataires.
    
- Prend en charge la méthode [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) . 
    
- Fournit du code pour la gestion des destinataires qui existent dans les conteneurs d'autres fournisseurs de carnet d'adresses appelés fournisseurs d'hôte. Ce code implique un objet Property, généralement une implémentation d'interface **IMAPIProp** , qui enveloppe un objet Property à partir du fournisseur hôte. 
    
Agir en tant que fournisseur étranger est un rôle facultatif; tous les fournisseurs n'ont pas besoin de prendre en charge les identificateurs de modèle et leur code associé. Implémentez votre fournisseur en tant que fournisseur étranger si vous souhaitez maintenir le contrôle des destinataires que les fournisseurs hôtes créent à l'aide de modèles fournis par votre fournisseur. 
  
Le format que votre fournisseur utilise pour ses identificateurs d'entrée peut également être utilisé pour ses identificateurs de modèle. Les identificateurs de modèle doivent inclure le **MAPIUID** enregistré de votre fournisseur pour permettre à MAPI de lier correctement les destinataires aux fournisseurs appropriés. 
  
MAPI appelle la méthode **IABLogon:: OpenTemplateID** de votre fournisseur lorsqu'un fournisseur d'hôte appelle [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md). Le fournisseur hôte transmet l'identificateur de modèle du destinataire dans le paramètre _lpTemplateID_ dans son appel à **IMAPISupport:: OpenTemplateID**. MAPI détermine que l'identificateur de modèle appartient à votre fournisseur en comparant le [MAPIUID](mapiuid.md) dans l'identificateur de modèle avec le **MAPIUID** que votre fournisseur a enregistré lors de l'ouverture de session. MAPI transfère ensuite l'appel du fournisseur de l'hôte à votre fournisseur via la méthode **IABLogon:: OpenTemplateID** . 
  
Le fournisseur hôte transmet également un pointeur à son implémentation d'objet de propriété pour le destinataire dans le paramètre _lpMAPIPropData_ , un identificateur d'interface dans le paramètre _lpInterface_ qui correspond au type d'implémentation de l'interface transmis dans _lpMAPIPropData_et un indicateur facultatif, FILL_ENTRY. Votre fournisseur est supposé renvoyer dans le paramètre _lppMAPIPropNew_ pointeur vers une implémentation d'objet de propriété du type spécifié dans _lpInterface_. Le pointeur renvoyé peut être soit à l'objet de propriété encapsulé implémenté par votre fournisseur, soit à l'objet fourni par le fournisseur hôte dans _lpMAPIPropData_. Votre fournisseur doit renvoyer un pointeur d'objet de propriété encapsulée lorsque:
  
- La table d'affichage du destinataire contient des contrôles de zone de liste.
    
- L'adresse de messagerie du destinataire doit être Assemblée à partir de données dans plusieurs contrôles de table d'affichage.
    
- Votre fournisseur émet des notifications de table d'affichage.
    
L'indicateur FILL_ENTRY indique à votre fournisseur que le fournisseur d'hôte requiert que toutes les propriétés du destinataire soient mises à jour. Votre fournisseur est nécessaire pour répondre à cette demande.
  
Lorsqu'un fournisseur hôte appelle la méthode **OpenTemplateID** de votre fournisseur, votre fournisseur peut: 
  
- Mettre à jour régulièrement les données d'une entrée copiée.
    
- Conserver une entrée copiée synchronisée avec son original, par exemple lorsqu'une entrée de carnet d'adresses est copiée dans le carnet d'adresses personnel.
    
- Implémenter des fonctionnalités qui ne peuvent pas être implémentées par le fournisseur hôte, telles que le remplissage dynamique de zones de liste dans la table des détails de l'entrée copiée à partir de données sur un serveur.
    
- Contrôler l'interaction entre les propriétés d'une entrée copiée ou d'un modèle instancié. Par exemple, calcul de **PR_EMAIL_ADDRESS** à partir d'autres propriétés affichées dans le tableau des détails. 
    
Les deux premiers éléments sont des exemples de tâches qui ne nécessitent pas que votre fournisseur fournisse un objet de propriété incluse, une implémentation de **IMAPIProp** basée sur l'implémentation du fournisseur de l'hôte. Votre fournisseur peut simplement mettre à jour les propriétés, le cas échéant, en définissant le paramètre _lppMAPIPropNew_ de sorte qu'il pointe vers le pointeur transmis par le fournisseur hôte dans le paramètre _lpMAPIPropData_ . 
  
Les deux tâches suivantes requièrent que votre fournisseur retourne au fournisseur hôte un objet Property qui encapsule l'objet du fournisseur d'hôte avec des fonctionnalités supplémentaires, telles que la possibilité d'afficher une feuille de propriétés pour l'entrée. Cet objet Property sera un utilisateur de messagerie ou une liste de distribution, selon le type d'objet transmis par le fournisseur d'hôte dans le paramètre _lpMAPIPropData_ et indiqué par l'identificateur d'interface dans le paramètre _lpInterface_ . Si le paramètre _lpMAPIPropData_ pointe vers un utilisateur de messagerie, l'objet de propriété encapsulé de votre fournisseur doit être une implémentation **IMailUser** . Si _lpMAPIPropData_ pointe vers une liste de distribution, il doit s'agir d'une implémentation **IDistList** . 
  
L'objet de propriété encapsulé de votre fournisseur intercepte les appels de la méthode **IMAPIProp** pour effectuer une manipulation spécifique du contexte du destinataire du fournisseur d'hôte, c'est-à-dire l'objet qu'il encapsule. MAPI n'a qu'une seule condition requise pour les objets de propriété encapsulés: tous les appels à [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) la demande de la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) doit être transmise au fournisseur d'hôte. L'implémentation de votre fournisseur peut utiliser la table renvoyée pour intercepter les notifications d'affichage de table ou ajouter ses propres notifications. 
  
La liste suivante inclut les tâches généralement implémentées dans l'objet de propriété encapsulé implémenté par des fournisseurs étrangers:
  
- Valeurs des propriétés de prétraitement et de post-traitement pour le destinataire hôte dans [IMAPIProp:: GetProps](imapiprop-getprops.md).
    
- Gestion des détails des contrôles d'affichage de tableau, tels que les boutons et les zones de liste, dans **IMAPIProp:: OpenProperty**.
    
- Validation ou manipulation des valeurs de propriété pour le destinataire hôte dans [IMAPIProp:: SetProps](imapiprop-setprops.md).
    
- Calculer les propriétés requises telles que **PR_EMAIL_ADDRESS** et vérifier que toutes les propriétés nécessaires ont été définies avant d'enregistrer le destinataire de l'hôte dans [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).
    
### <a name="to-implement-iablogonopentemplateid"></a>Pour implémenter IABLogon:: OpenTemplateID
  
1. Vérifiez si l'identificateur de modèle passé avec le paramètre _lpTemplateID_ est valide et s'il est dans un format reconnu par votre fournisseur. Si ce n'est pas le cas, échec et renvoyer MAPI_E_INVALID_ENTRYID. 
    
2. Créez un objet du type indiqué par l'identificateur de modèle, un utilisateur de messagerie, une liste de distribution ou un destinataire isolé. 
    
3. Appelez la méthode **IUnknown:: AddRef** dans l'objet Property du fournisseur hôte, qui est l'objet désigné par le paramètre _lpMAPIPropData_ . 
    
4. Si le paramètre _ulTemplateFlags_ est défini sur FILL_ENTRY: 
    
   1. Si le nouvel objet est un utilisateur de messagerie ou une liste de distribution:
      
      1. Récupérez toutes les propriétés du nouvel objet, éventuellement en appelant sa méthode **IMAPIProp:: GetProps** . 
          
      2. Appelez la méthode **IMAPIProp:: SetProps** du fournisseur hôte pour copier toutes les propriétés récupérées dans l'objet Property du fournisseur hôte. 
      
   2. Si le nouvel objet est un destinataire isolé, appelez la méthode **IMAPIProp:: SetProps** du fournisseur hôte pour définir les propriétés suivantes: 
      
      - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) vers le type d'adresse géré par votre fournisseur.
        
      - **PR\_TemplateID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) à l'identificateur de modèle à partir des paramètres _lpTemplateID_ et _cbTemplateID_ . 
        
      - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) à DT_MAILUSER ou DT_DISTLIST, selon le cas.
    
5. Définissez le contenu du paramètre _lppMAPIPropNew_ de sorte qu'il pointe vers le nouvel objet de votre fournisseur ou l'objet Property transmis avec le paramètre _lpMAPIPropData_ , selon que votre fournisseur détermine ou non un objet encapsulé. 
    
6. Si une erreur critique se produit, comme une défaillance réseau ou une condition de mémoire insuffisante, renvoyez la valeur d'erreur appropriée. Cette valeur doit être propagée au client avec la structure [MAPIERROR](mapierror.md) appropriée, une tâche effectuée par le fournisseur de l'hôte. 
    

