---
title: XML pour les amis
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3362639a-8098-47ab-ba94-ee89e4920032
description: L'élément Friends du schéma XML du fournisseur Microsoft Outlook Social Connector (OSC) permet à un fournisseur OSC de spécifier des informations pour une liste de personnes associées à un utilisateur Outlook dans le réseau social.
ms.openlocfilehash: df3bf03c5fd1dcdac3096411bc60bcb1eeec661e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361158"
---
# <a name="xml-for-friends"></a>XML pour les amis

L' **** élément Friends du schéma XML du fournisseur Microsoft Outlook Social Connector (OSC) permet à un fournisseur OSC de spécifier des informations pour une liste de personnes associées à un utilisateur Outlook dans le réseau social. Si le fournisseur OSC prend en charge la synchronisation mise en cache, cette liste de personnes ne contiendra que les amis de l'utilisateur Outlook sur le réseau social. Si OSC prend en charge la synchronisation à la demande ou hybride, cette liste peut contenir à la fois des amis et des non-Friends de l'utilisateur Outlook. 

Chaque membre de la liste est représenté comme un élément **Person** dans le schéma XML, qui prend en charge des informations telles que le prénom, le nom et les adresses de messagerie. Les fournisseurs OSC utilisent **** les éléments Friend et **Person** indépendamment de la façon dont ils veulent que OSC synchronise les informations des amis à partir du réseau social. Notez que les éléments enfants de **Person** sont semblables à certaines propriétés d'un contact Outlook, ce qui facilite le stockage des amis dans un dossier de contacts Outlook spécifique au réseau social, si le réseau social prend en charge la mise en cache ou l'environnement hybride. synchronisation des amis avec un dossier de contacts Outlook. 

## <a name="example-scenarios"></a>Exemples de scénarios

Les exemples de scénarios suivants illustrent les appels de l'API de l'extensibilité du fournisseur OSC qu'un fournisseur OSC implémente et l'interface OSC pour obtenir des informations sur les amis. Les informations sont exprimées dans des chaînes XML conformes au schéma XML du fournisseur OSC.
  
Pour obtenir un exemple d'amis XML, consultez la rubrique [Friend XML example](friends-xml-example.md). Pour plus d'informations sur la synchronisation des informations des amis, consultez la rubrique [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).

### <a name="scenario-1-get-a-list-of-friends"></a>Scénario 1: obtenir une liste d'amis

Scénario 1: OSC Obtient une liste d'amis, un objet [ISocialPerson](isocialpersoniunknown.md) et une image pour chaque ami: 
    
1. Un fournisseur OSC qui prend en charge l'affichage des amis à partir du site du réseau social et permet à l'élément OSC de mettre en cache les informations Friend indique qu'à OSC à l'aide des éléments **getFriends** et **cacheFriends** , qui sont des éléments enfants du ** élément Capabilities** . 
    
2. Le fournisseur OSC implémente également les méthodes [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md), [ISocialSession:: GetPerson](isocialsession-getperson.md), [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)et [ISocialPerson:: GetPicture,](isocialperson-getpicture.md) . 
    
3. L'option OSC appelle **ISocialProvider:: GetCapabilities** pour vérifier la valeur des éléments suivants: **getFriends** pour vérifier que le fournisseur OSC prend en charge l'affichage des amis à partir du réseau social et **cacheFriends** pour vérifier que le fournisseur prend en charge la mise en cache des amis. 
    
4. Le OSC appelle **ISocialSession:: GetPerson** pour obtenir un objet **ISocialPerson** pour l'utilisateur Outlook. 
    
5. Le OSC appelle **ISocialPerson:: GetFriendsAndColleagues** pour obtenir la liste des amis de l'utilisateur Outlook renvoyée dans la chaîne de paramètre _personCollection_ . La chaîne _personCollection_ est conforme à la définition de schéma XML pour l'élément **Friends** dans le schéma XML. 
    
6. Pour chaque Friend dans la chaîne XML _personCollection_ , le OSC Obtient la valeur de l'élément **userid** pour appeler **ISocialSession:: GetPerson** afin d'obtenir un objet **ISocialPerson** pour cet ami. 
    
7. Pour chaque ami dans la chaîne XML **personCollection** , l'OSC appelle [ISocialPerson:: GetPicture,](isocialperson-getpicture.md) pour obtenir une ressource image pour cet ami. 
    
   Le OSC peut effectuer des appels supplémentaires sur l'objet **ISocialPerson** pour obtenir des activités et des détails (par exemple, des adresses de messagerie) pour cet ami. 
    
### <a name="scenario-2-synchronize-friends"></a>Scénario 2: synchroniser des amis 

Scénario 2: OSC synchronise les amis de manière dynamique:
    
1. Un fournisseur OSC qui prend en charge la synchronisation à la demande des amis et des non-amis indique qu'à OSC à l'aide des éléments **getFriends** et **dynamicContactsLookup** . Le fournisseur OSC définit également l'élément **hashFunction** . Les trois éléments sont des éléments enfants des **fonctionnalités**. 
    
2. Le fournisseur OSC implémente également la méthode [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md) . 
    
3. L'option OSC appelle **ISocialProvider:: GetCapabilities** pour vérifier les valeurs de **getFriends** et de **dynamicContactsLookup** afin de vérifier que le fournisseur OSC prend en charge la synchronisation des amis et des amis et des non-amis. Le OSC prend également note de la valeur de **hashFunction** prise en charge par le fournisseur OSC. 
    
4. Pour chaque utilisateur affiché dans le volet de personnes, le OSC recueille l'adresse de messagerie de l'utilisateur et la chiffre à l'aide de la fonction de hachage spécifiée dans **hashFunction**. Il s'agit d'une chaîne XML conforme à la définition de schéma XML pour l'élément **hashedAddresses** . 
    
5. L'OSC appelle **ISocialSession2:: GetPeopleDetails**, en fournissant cette chaîne XML d'adresses hachées comme paramètre _personAddresses_ , afin d'obtenir dynamiquement les détails mis à jour pour les personnes dans le paramètre _personsCollection_ . La chaîne de paramètre _personsCollection_ est conforme à la définition de schéma XML pour l'élément **Friends** dans le schéma XML. 

## <a name="parent-and-child-elements"></a>Éléments parents et enfants

Les éléments suivants sont les deux éléments de niveau supérieur dans **** le schéma Friends. 
  
|**Élément**|**Description**|
|:-----|:-----|
|**camarade** <br/> |Représente l'élément racine d'une liste d'éléments **Person** . Les **ISocialPerson:: GetFriendsAndColleagues**, [ISocialSession:: FindPerson](isocialsession-findperson.md)et **ISocialSession2:: GETPEOPLEDETAILS** renvoient des chaînes XML conformes à la définition de schéma de **** l'élément Friends.  <br/> |
|**person** <br/> |Représente une personne dans une liste d'éléments **Person** . La méthode [ISocialPerson:: GetDetails](isocialperson-getdetails.md) renvoie une chaîne XML conforme à la définition de schéma de l'élément **Person** .  <br/> |
   
Le tableau suivant décrit chaque élément enfant de l'élément **Person** dans le schéma XML du fournisseur OSC. 
  
Pour obtenir une définition complète du schéma XML du fournisseur OSC, y compris les éléments requis ou facultatifs, voir [schéma XML du fournisseur Outlook Social Connector](outlook-social-connector-provider-xml-schema.md).
  
|**Élément**|**Description**|
|:-----|:-----|
|**adresse** <br/> |Adresse physique de la personne.  <br/> |
|**è** <br/> |Date anniversaire de mariage d'un événement pour la personne.  <br/> |
|**askmeabout** <br/> |Rubriques d'intérêt ou d'expertise de la personne.  <br/> |
|**t'** <br/> |Date de naissance de la personne.  <br/> |
|**businessAddress** <br/> |Adresse physique de l'espace de travail de la personne.  <br/> |
|**businessCity** <br/> |Ville du lieu de travail de la personne.  <br/> |
|**businessCountryOrRegion** <br/> |Pays ou région du lieu de travail de la personne.  <br/> |
|**businessState** <br/> |Département ou région du lieu de travail de la personne.  <br/> |
|**businessZip** <br/> |Code postal du lieu de travail de la personne.  <br/> |
|**Cell** <br/> |Numéro de téléphone mobile de la personne.  <br/> |
|**Mexico** <br/> |Ville de l'adresse physique de la personne.  <br/> |
|**company** <br/> |Nom de la société associée à la personne.  <br/> |
|**countryOrRegion** <br/> |Pays ou région de l'adresse physique de la personne.  <br/> |
|**creationTime** <br/> |Heure de création du profil de la personne sur le réseau social.  <br/> |
|**emailAddress** <br/> |Adresse de messagerie principale de la personne.  <br/> |
|**emailAddress2** <br/> |Adresse de messagerie secondaire de la personne.  <br/> |
|**emailAddress3** <br/> |Adresse de messagerie tertiaire de la personne.  <br/> |
|**expirationTime** <br/> |Heure à laquelle les données de profil de la personne arrivent à expiration sur le réseau social.  <br/> |
|**FileAs,** <br/> |Chaîne par laquelle la personne doit être classée en tant que contact dans un fichier de contacts Outlook.  <br/> |
|**firstName** <br/> |Prénom ou nom donné de la personne.  <br/> |
|**friendStatus** <br/> |Statut d'ami de cette personne avec l'utilisateur connecté sur le réseau social. Doit être l'une des valeurs suivantes: **Friend**, not **Friend**, **Pending**, **Pending**, **pendingout**.  <br/> |
|**NomComplet** <br/> |Nom complet de la personne.  <br/> |
|**femmes** <br/> |Sexe de la personne. Doit être l'une des valeurs suivantes: **mâle**, **femelle**, **non spécifié**.  <br/> |
|**homePhone** <br/> |Numéro de téléphone personnel de la personne.  <br/> |
|**index** <br/> |Emplacement de l'adresse hachée de la personne dans le paramètre de chaîne _personsAddresses_ transmis à un appel à la méthode **ISocialSession2:: GetPeopleDetails** . Il indique également le code XML **** de la personne dans la chaîne _personsCollection_ renvoyée par **GetPeopleDetails**.  <br/> |
|**artisanat** <br/> |Secteurs d'activité de la personne.  <br/> |
|**interests** <br/> |Centres d'intérêt ou loisirs de la personne.  <br/> |
|**lastModificationTime** <br/> |Heure de la dernière modification du profil de la personne sur le réseau social.  <br/> |
|**lastName** <br/> |Nom de famille ou prénom de la personne.  <br/> |
|**location** <br/> |Emplacement de la personne.  <br/> |
|**Pseudonym** <br/> |Nom plus court ou nom de fantaisie de la personne.  <br/> |
|**OtherAddress,** <br/> |Autre adresse postale de la personne.  <br/> |
|**otherCity** <br/> |Ville de l'adresse de remplacement de la personne.  <br/> |
|**otherCountryOrRegion** <br/> |Pays ou région de l'adresse de remplacement de la personne.  <br/> |
|**otherState** <br/> |Département ou région de l'adresse de remplacement de la personne.  <br/> |
|**otherZip** <br/> |Code postal de l'adresse de remplacement de la personne.  <br/> |
|**téléphonique** <br/> |Numéro de téléphone principal de la personne.  <br/> |
|**pictureUrl** <br/> |URL d'une image de profil de la personne.  <br/> |
|**rapports** <br/> |Relation de cette personne avec l'utilisateur connecté.  <br/> |
|**scolaire** <br/> |Les écoles vers lesquelles la personne passe ou accède.  <br/> |
|**skills** <br/> |Compétences personnelles de la personne.  <br/> |
|**state** <br/> |Département ou région de l'adresse physique de la personne.  <br/> |
|**title** <br/> |Désignation ajoutée au nom de la personne.  <br/> |
|**Identifi** <br/> |ID permettant d'identifier la personne sur le réseau social.  <br/> |
|**webProfilePage** <br/> |Adresse de la page Web qui contient un profil de la personne.  <br/> |
|**redefinery** <br/> |Site Web de la personne.  <br/> |
|**workPhone** <br/> |Numéro de téléphone professionnel de la personne.  <br/> |
|**ville** <br/> |Code postal de l'adresse physique de la personne.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Exemple de code XML pour les amis](friends-xml-example.md)  
- [Synchronisation des amis et des activités](synchronizing-friends-and-activities.md)  
- [XML pour les fonctionnalités](xml-for-capabilities.md) 
- [XML pour les activités](xml-for-activities.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

