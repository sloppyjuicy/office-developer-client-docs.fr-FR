---
title: Création d’un destinataire
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 586c901f-d9f9-44f2-a328-051775a81265
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c596cb219cb1096f186e616c05b8372fef3b42a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783116"
---
# <a name="creating-a-recipient"></a>Création d’un destinataire

  
  
**S’applique à**: Outlook 
  
Clients de créer des destinataires lors de l’envoi de messages et lorsqu’ils sont Ajout d’entrées pour les conteneurs de carnet d’adresses modifiable. MAPI propose trois méthodes pour la création de destinataires :
  
- [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
    
- [IAddrBook::NewEntry](iaddrbook-newentry.md)
    
- [IABContainer::CreateEntry](iabcontainer-createentry.md)
    
Appelez **IAddrBook::CreateOneOff** lorsque vous créez des destinataires à utiliser pour envoyer des messages. **CreateOneOff** crée un identificateur d’entrée unique mise en forme spéciale pour être associé à une adresse d’un type particulier. Pour plus d’informations sur uniques et les identificateurs d’entrée unique, voir [Adresses uniques](one-off-addresses.md) et des [Identificateurs uniques d’entrée](one-off-entry-identifiers.md).
  
Appel **IAddrBook::NewEntry** lorsque vous créez des destinataires à être utilisé pour envoyer des messages ou à ajouter à un conteneur. **NewEntry** a trois paires de paramètres qui contiennent les identificateurs d’entrée. Ces paramètres sont décrits comme suit : 
  
|**Paire de paramètre**|**Description**|
|:-----|:-----|
| _cbEidContainer_ et _lpEidContainer_ <br/> |Identificateur d’entrée pour le conteneur dans lequel la nouvelle entrée doit être placée.  <br/> |
| _cbEidNewEntryTpl_ et _lpEidNewEntryTpl_ <br/> |Identificateur d’entrée pour le modèle à utiliser pour créer la nouvelle entrée.  <br/> |
| _lpcbEidNewEntry_ et _lppEidNewEntry_ <br/> |Identificateur d’entrée pour la nouvelle entrée.  <br/> |
   
Pour créer un destinataire d’un message sortant, définissez _cbEidContainer_ à zéro et _lpEidContainer_ sur NULL. **NewEntry** crée un destinataire avec un identificateur d’entrée est conforme au format unique, le même type de destinataire qui est généré par un appel à **IAddrBook::CreateOneOff**. 
  
Pour créer un destinataire à insérer dans un conteneur particulier, définissez _lpEidContainer_ du conteneur identificateur d’entrée et _cbEidContainer_ pour le nombre d’octets dans l’identificateur d’entrée du conteneur. 
  
Pour utiliser un modèle pour créer un destinataire, définissez _lpEidNewEntryTpl_ sur l’identificateur d’entrée du modèle à utiliser et _cbEidNewEntryTpl_ au nombre d’octets dans cet identificateur d’entrée. Plus des conteneurs du carnet d’adresses modifiable prend en charge un ou plusieurs modèles pour créer des entrées d’un type particulier. Modèles uniques sont généralement, mais pas toujours, boîtes de dialogue. Entrer des informations dans le modèle de produit un destinataire dont l’adresse est correctement mis en forme pour le type. 
  
Obtenir l’identificateur d’entrée modèle soit :
  
- La colonne **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) dans la table uniques du conteneur, accédé à l’appel de méthode [d’IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur et en spécifiant **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) en tant que la balise de propriété et IID_IMAPITable en tant que l’identificateur d’interface. 
    
- Un carnet d’adresses **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) du fournisseur et des propriétés **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) qui contiennent les identificateurs d’entrée pour le fournisseur de messagerie de l’objet utilisateur et modèles de liste de distribution. 
    
> [!NOTE]
> Ne confondez pas l’identificateur d’entrée d’un nouveau modèle entrée avec un autre type d’identificateur d’entrée appelé un identificateur de modèle. Un identificateur de modèle est utilisé par les fournisseurs pour gérer les entrées copiées à partir d’autres fournisseurs ; Il n’est jamais utilisé par les clients et il n’est pas utilisé pour créer de nouvelles entrées. 
  
Pour permettre à l’utilisateur déterminer le type d’entrée à créer, passez zéro pour _cbEidNewEntryTpl_ et NULL pour _lpEidNewEntryTpl_. Lorsque cela se produit, **NewEntry** affiche une boîte de dialogue commune construite à partir unique table de MAPI, une liste hiérarchique de tous les modèles pris en charge par chaque fournisseur de carnet d’adresses dans le profil. 
  
Lorsqu’un type d’adresse a été déterminé, soit par le biais du paramètre du paramètre _lpEidNewEntryTpl_ ou une sélection par l’utilisateur à partir de l’affichage tableau uniques, **NewEntry** affiche le modèle correspondant à l’aide de son affichage de la table. Tous les nouveaux modèles d’entrée prend en charge la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). 
  
Pour renvoyer l’identificateur d’entrée de l’entrée créée **NewEntry** , transmettez une adresse valide pour les paramètres _lpcbEidNewEntry_ et _lppEidNewEntry_ . MAPI place l’identificateur d’entrée à l’adresse vers laquelle pointé _lppEidNewEntry_ et le nombre d’octets du nouvel identificateur d’entrée à l’adresse vers laquelle pointé _lpcbEidNewEntry_.
  
Appelez [IABContainer::CreateEntry](iabcontainer-createentry.md) pour créer un destinataire et enregistrez-le dans un conteneur de carnet d’adresses particulière. Vous pouvez utiliser cette méthode uniquement avec les conteneurs modifiables : conteneurs dont la AB_MODIFIABLE l’indicateur est défini dans leur propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)). Fournisseurs de carnet d’adresses avec des conteneurs non modifiables ne prennent pas en charge cette méthode. Spécifier l’identificateur d’entrée du modèle pour la création d’une entrée du type souhaité dans le paramètre _lpEntryID_ . 
  
Dans le paramètre _ulCreateFlags_ , spécifiez le type d’entrée en double vérification obligatoire et ou non les nouvelles entrées doivent remplacer existants. Si **CreateEntry** ne parvient pas à créer un nouvel objet en raison de la vérification de l’entrée en double imposées par le fournisseur, pas vous devriez voir une erreur ou un avertissement renvoyé. Dans ces conditions, fournisseurs retournent un code de réussite. 
  
Si vous travaillez directement avec un conteneur et que vous savez exactement les types d’adresses que le conteneur peut créer, vous pouvez appeler **IABContainer::CreateEntry** et transmettre l’identificateur d’entrée pour le modèle approprié. Le fournisseur de carnet d’adresses définit certaines propriétés par défaut ; Vous pouvez appeler **SetProps** pour définir d’autres personnes. L’utilisateur n’est jamais concerné. 
  

