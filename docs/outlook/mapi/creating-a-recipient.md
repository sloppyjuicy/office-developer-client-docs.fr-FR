---
title: Création d’un destinataire
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 586c901f-d9f9-44f2-a328-051775a81265
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a237cc5b04f80d12713d6b3d136ab755a9fe5d05
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62461376"
---
# <a name="creating-a-recipient"></a>Création d’un destinataire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients créent des destinataires lorsqu’ils adressent des messages et lorsqu’ils ajoutent des entrées à des conteneurs de carnet d’adresses modifiables. MAPI fournit trois méthodes pour créer des destinataires :
  
- [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
    
- [IAddrBook::NewEntry](iaddrbook-newentry.md)
    
- [IABContainer::CreateEntry](iabcontainer-createentry.md)
    
**Appelez IAddrBook::CreateOneOff** lorsque vous créez des destinataires à utiliser pour traiter les messages. **CreateOneOff** crée un identificateur d’entrée unique spécialement formaté à associer à une adresse d’un type d’adresse particulier. Pour plus d’informations sur les identificateurs d’entrée uniques et uniques, voir [Adresses](one-off-addresses.md) uniques et Identificateurs d’entrée [uniques](one-off-entry-identifiers.md).
  
**Appelez IAddrBook::NewEntry** lorsque vous créez des destinataires à utiliser pour traiter des messages ou pour les ajouter à un conteneur. **NewEntry possède** trois paires de paramètres qui contiennent des identificateurs d’entrée. Ces paramètres sont décrits comme suit : 
  
|**Paire de paramètres**|**Description**|
|:-----|:-----|
| _cbEidContainer_ et  _lpEidContainer_ <br/> |Identificateur d’entrée pour le conteneur dans lequel la nouvelle entrée doit être placée.  <br/> |
| _cbEidNewEntryTpl_ et  _lpEidNewEntryTpl_ <br/> |Identificateur d’entrée du modèle à utiliser pour créer la nouvelle entrée.  <br/> |
| _lpcbEidNewEntry_ et  _lppEidNewEntry_ <br/> |Identificateur d’entrée de la nouvelle entrée.  <br/> |
   
Pour créer un destinataire pour un message sortant, définissez  _cbEidContainer_ sur zéro et  _lpEidContainer_ sur NULL. **NewEntry** crée un destinataire avec un identificateur d’entrée conforme au format unique, le même type de destinataire produit par un appel à **IAddrBook::CreateOneOff**. 
  
Pour créer un destinataire à insérer dans un conteneur particulier, définissez  _lpEidContainer_ sur l’identificateur d’entrée du conteneur et  _cbEidContainer_ sur le nombre d’octets dans l’identificateur d’entrée du conteneur. 
  
Pour utiliser un modèle pour créer un destinataire, définissez  _lpEidNewEntryTpl_ sur l’identificateur d’entrée du modèle à utiliser et  _cbEidNewEntryTpl_ sur le nombre d’octets dans cet identificateur d’entrée. La plupart des conteneurs de carnet d’adresses modifiables peuvent prendre en charge un ou plusieurs modèles pour la création d’entrées d’un type particulier. Les modèles unique sont généralement, mais pas toujours, des boîtes de dialogue. La saisie d’informations dans le modèle produit un destinataire avec une adresse correctement mise en forme pour le type. 
  
Obtenez l’identificateur d’entrée de modèle de l’une des façons ci-après :
  
- Colonne **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) dans la table unique du conteneur, accessible en appelant la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur et en spécifiant **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) comme balise de propriété et IID_IMAPITable comme identificateur d’interface. 
    
- Propriétés **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) et **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) d’un fournisseur de carnet d’adresses qui détiennent les identificateurs d’entrée pour l’objet utilisateur de messagerie et les modèles de liste de distribution du fournisseur. 
    
> [!NOTE]
> Ne confondez pas l’identificateur d’entrée d’un nouveau modèle d’entrée avec un autre type d’identificateur d’entrée appelé identificateur de modèle. Un identificateur de modèle est utilisé uniquement par les fournisseurs pour conserver les entrées copiées à partir d’autres fournisseurs ; Il n’est jamais utilisé par les clients et n’est pas utilisé pour créer de nouvelles entrées. 
  
Pour permettre à l’utilisateur de déterminer le type d’entrée à créer, passez zéro pour  _cbEidNewEntryTpl_ et NULL pour  _lpEidNewEntryTpl_. Lorsque cela se produit, **NewEntry** affiche une boîte de dialogue commune conçue à partir de la table unique MAPI , une liste hiérarchique de tous les modèles pris en charge par chaque fournisseur de carnet d’adresses dans le profil. 
  
Lorsqu’un type d’adresse a été déterminé, soit par le paramètre  _lpEidNewEntryTpl_ , soit par une sélection de l’utilisateur dans l’affichage de tableau unique, **NewEntry** affiche le modèle correspondant à l’aide de sa table d’affichage. Tous les nouveaux modèles d’entrées **PR_DETAILS_TABLE** la propriété ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). 
  
Pour que **NewEntry** retourne l’identificateur d’entrée de l’entrée créée, passez une adresse valide pour les paramètres  _lpcbEidNewEntry_ et  _lppEidNewEntry_ . MAPI place le nouvel identificateur d’entrée à l’adresse pointée par  _lppEidNewEntry_ et le nombre d’byte du nouvel identificateur d’entrée à l’adresse pointée par  _lpcbEidNewEntry_.
  
[Appelez IABContainer::CreateEntry](iabcontainer-createentry.md) pour créer un destinataire et l’enregistrer dans un conteneur de carnet d’adresses particulier. Vous pouvez utiliser cette méthode uniquement avec des conteneurs modifiables — conteneurs dont l’indicateur AB_MODIFIABLE est définie dans leur propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)). Les fournisseurs de carnets d’adresses avec conteneurs nonmodifiables ne peuvent pas prendre en charge cette méthode. Spécifiez l’identificateur d’entrée du modèle pour créer une entrée du type souhaité dans _le paramètre lpEntryID_ . 
  
Dans le  _paramètre ulCreateFlags_ , spécifiez le type de vérification des entrées en double requis et indiquez si les nouvelles entrées doivent remplacer les entrées existantes. Si **CreateEntry** ne parvient pas à créer un objet en raison de la vérification des entrées en double imposée par le fournisseur, ne vous attendez pas à voir une erreur ou un avertissement renvoyé. Dans ces conditions, les fournisseurs retournent un code de réussite. 
  
Si vous travaillez directement avec un conteneur et que vous connaissez exactement les types d’adresses que le conteneur peut créer, vous pouvez appeler **IABContainer::CreateEntry** et transmettre l’identificateur d’entrée pour le modèle approprié. Le fournisseur de carnet d’adresses définit certaines propriétés par défaut initiales . vous pouvez appeler **SetProps pour** en définir d’autres. L’utilisateur n’est jamais impliqué. 
  

