---
title: Code XML des amis
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3362639a-8098-47ab-ba94-ee89e4920032
description: L’élément amis dans le schéma XML du fournisseur Microsoft Outlook Social Connector (OSC) permet à un fournisseur OSC spécifier des informations pour une liste de personnes associées à un utilisateur d’Outlook dans le réseaux sociaux.
ms.openlocfilehash: 07f1bb77e7912e3973fd2af8a70275642b72039c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787731"
---
# <a name="xml-for-friends"></a>Code XML des amis

L’élément **amis** dans le schéma XML du fournisseur Microsoft Outlook Social Connector (OSC) permet à un fournisseur OSC spécifier des informations pour une liste de personnes associées à un utilisateur d’Outlook dans le réseaux sociaux. Si le fournisseur OSC prend en charge la synchronisation mis en cache, cette liste de personne contient uniquement des amis de l’utilisateur Outlook sur le réseaux sociaux. Si l’OSC prend en charge la synchronisation de la demande ou hybrides, cette liste peut contenir des amis et non amis de l’utilisateur d’Outlook. 

Chaque personne dans la liste est représenté comme un élément de la **personne** dans le schéma XML, qui prend en charge les détails tels que Prénom, nom de famille et les adresses de messagerie. Fournisseurs OSC utilisent les éléments de **vos amis** et **personne** quelle que soit la façon dont ils souhaitent l’OSC de synchroniser les informations ami à partir du réseau social. Notez que les éléments enfants de la **personne** sont similaires à certains de ces propriétés d’un contact Outlook, ce qui facilite le stockage amis dans un dossier de contacts Outlook spécifique au réseau social, si la mise en cache de la prise en charge de réseaux sociaux ou hybrides synchronisation des contacts dans un dossier de contacts Outlook. 

## <a name="example-scenarios"></a>Exemples de scénarios

Les exemples de scénarios suivants montrent le fournisseur OSC appels API d’extensibilité qui implémente un fournisseur OSC et l’OSC permet d’obtenir des informations ami. Informations sont exprimées dans des chaînes de code XML conforme au schéma XML OSC fournisseur.
  
Pour obtenir un exemple d’amis XML, voir [Exemple de code XML amis](friends-xml-example.md). Pour plus d’informations sur la synchronisation des informations de vos amis, voir [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).

### <a name="scenario-1-get-a-list-of-friends"></a>Scénario 1 : obtenir une liste d’amis

Scénario 1 : OSC Obtient la liste des amis et un objet [ISocialPerson](isocialpersoniunknown.md) et une image pour chacun d'entre eux : 
    
1. Un fournisseur OSC qui prend en charge affichant des amis à partir du site de réseau social et en autorisant que l’OSC en cache les informations ami qui indique à l’OSC en utilisant les éléments **getFriends** et **cacheFriends** , qui sont des éléments enfants de le ** fonctionnalités** élément. 
    
2. Le fournisseur OSC implémente également la [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), [ISocialSession::GetPerson](isocialsession-getperson.md), [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)et méthodes [ISocialPerson::GetPicture](isocialperson-getpicture.md) . 
    
3. L’OSC appelle **ISocialProvider::GetCapabilities** pour vérifier la valeur des éléments suivants : **getFriends** pour vérifier que le fournisseur OSC prend en charge les affichant des amis ou des réseaux sociaux et **cacheFriends** pour vérifier que le fournisseur prend en charge la mise en cache des amis. 
    
4. L’OSC appelle **ISocialSession::GetPerson** pour obtenir un objet **ISocialPerson** pour l’utilisateur d’Outlook. 
    
5. L’OSC appelle **ISocialPerson::GetFriendsAndColleagues** pour obtenir de l’utilisateur Outlook de liste d’amis renvoyé dans la chaîne de paramètre _personCollection_ . La chaîne _personCollection_ est conforme à la définition de schéma XML pour l’élément **amis** dans le schéma XML. 
    
6. Pour chacun d'entre eux dans la chaîne XML _personCollection_ , l’OSC Obtient la valeur de l’élément **userID** pour appeler **ISocialSession::GetPerson** pour obtenir un objet **ISocialPerson** pour ce ami. 
    
7. Pour chacun d'entre eux dans la chaîne XML **personCollection** , l’OSC appelle [ISocialPerson::GetPicture](isocialperson-getpicture.md) pour obtenir une ressource d’image de cet expéditeur. 
    
   L’OSC pouvez émettre des appels sur l’objet **ISocialPerson** pour obtenir plus d’informations (par exemple, les adresses de messagerie) et les activités supplémentaires pour ce ami. 
    
### <a name="scenario-2-synchronize-friends"></a>Scénario 2 : synchroniser vos amis 

Scénario 2 : OSC synchronise amis dynamiquement :
    
1. Un fournisseur OSC qui prend en charge la synchronisation de la demande de vos amis et non amis qui indique à l’OSC en utilisant les éléments **getFriends** et **dynamicContactsLookup** . Le fournisseur OSC définit également l’élément **hashFunction** . Tous les trois éléments sont des éléments enfants de **fonctionnalités**. 
    
2. Le fournisseur OSC implémente également la méthode [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) . 
    
3. L’OSC appelle **ISocialProvider::GetCapabilities** pour vérifier les valeurs de **getFriends** et **dynamicContactsLookup** pour vérifier que le fournisseur OSC prend en charge des amis et à la demande sur la synchronisation des amis et non amis. L’OSC permet également de note de la valeur de **hashFunction** pris en charge par le fournisseur OSC. 
    
4. Pour chaque utilisateur affiché dans le volet personnes, l’OSC collecte d’adresse de messagerie de l’utilisateur et le chiffre à l’aide de la fonction de hachage spécifiée dans **hashFunction**. Ceci constitue une chaîne XML qui est conforme à la définition de schéma XML pour l’élément **hashedAddresses** . 
    
5. L’OSC appelle **ISocialSession2::GetPeopleDetails**, fournir cette chaîne XML des adresses de hachage en tant que paramètre _personAddresses_ , pour obtenir dynamiquement des mises à jour pour les personnes dans le paramètre _personsCollection_ . La chaîne du paramètre _personsCollection_ est conforme à la définition de schéma XML pour l’élément **amis** dans le schéma XML. 

## <a name="parent-and-child-elements"></a>Éléments parents et enfants

Voici les deux éléments de niveau supérieur dans le schéma de **vos amis** . 
  
|**Élément**|**Description**|
|:-----|:-----|
|**amis** <br/> |Représente l’élément racine d’une liste d’éléments de la **personne** . Le **ISocialPerson::GetFriendsAndColleagues**, [ISocialSession::FindPerson](isocialsession-findperson.md)et **ISocialSession2::GetPeopleDetails** renvoient des chaînes XML conforme à la définition de schéma de l’élément **amis** .  <br/> |
|**person** <br/> |Représente une personne dans une liste d’éléments de la **personne** . La méthode [ISocialPerson::GetDetails](isocialperson-getdetails.md) renvoie une chaîne XML qui est conforme à la définition de schéma de l’élément de la **personne** .  <br/> |
   
Le tableau suivant décrit chaque élément enfant de l’élément de la **personne** dans le schéma XML du fournisseur OSC. 
  
Pour une définition complète du schéma XML de fournisseur OSC, y compris les éléments qui sont obligatoires ou facultatives, voir [Schéma du XML fournisseur Outlook Social Connector](outlook-social-connector-provider-xml-schema.md).
  
|**Élément**|**Description**|
|:-----|:-----|
|**adresse** <br/> |Adresse postale physique de la personne.  <br/> |
|**Anniversaire de mariage** <br/> |Date anniversaire pour un événement de la personne.  <br/> |
|**askmeabout** <br/> |Rubriques des intérêts ou des compétences de la personne.  <br/> |
|**Anniversaire** <br/> |Date de naissance de la personne.  <br/> |
|**businessAddress** <br/> |Adresse postale physique de l’espace de travail de la personne.  <br/> |
|**Ville (bureau)** <br/> |Ville de l’espace de travail de la personne.  <br/> |
|**businessCountryOrRegion** <br/> |Pays ou région de l’espace de travail de la personne.  <br/> |
|**businessState** <br/> |État ou province de l’espace de travail de la personne.  <br/> |
|**businessZip** <br/> |ZIP ou le code postal de l’espace de travail de la personne.  <br/> |
|**cellule** <br/> |Numéro de téléphone mobile de la personne.  <br/> |
|**Ville** <br/> |Ville de l’adresse physique de la personne.  <br/> |
|**société** <br/> |Nom de la société associée à la personne.  <br/> |
|**countryorregion définit** <br/> |Pays ou région de l’adresse physique de la personne.  <br/> |
|**creationTime** <br/> |Heure de création du profil de la personne sur le réseau social.  <br/> |
|**emailAddress** <br/> |Adresse de messagerie principale de la personne.  <br/> |
|**emailAddress2** <br/> |Adresse de messagerie secondaire de la personne.  <br/> |
|**emailAddress3** <br/> |Adresse de messagerie de troisième rang de la personne.  <br/> |
|**expirationTime** <br/> |Heure d’expirent des données de profil de la personne sur le réseau social.  <br/> |
|**Classer sous** <br/> |Chaîne à laquelle la personne doit être classé comme un contact dans Outlook fichier de contacts.  <br/> |
|**firstName** <br/> |Prénom ou prénom de la personne.  <br/> |
|**friendStatus** <br/> |État ami de cette personne à l’utilisateur ayant ouvert une session sur le réseau social. Doit être une des valeurs suivantes : **ami**, **nonfriend**, **en attente**, **pendingin**, **pendingout**.  <br/> |
|**fullName** <br/> |Nom complet de la personne.  <br/> |
|**sexe** <br/> |Sexe de la personne. Doit être une des valeurs suivantes : **masculin**, **féminin**, **non spécifié**.  <br/> |
|**homePhone** <br/> |Numéro de téléphone personnel de la personne.  <br/> |
|**index** <br/> |Emplacement de l’adresse de hachage de la personne dans le paramètre de chaîne _personsAddresses_ passés à un appel à la méthode **ISocialSession2::GetPeopleDetails** . Il indique également **personne** XML dans la chaîne _personsCollection_ retournée par **GetPeopleDetails la personne à**.  <br/> |
|**secteurs d’activité** <br/> |Secteurs la personne participe à.  <br/> |
|**centres d’intérêt** <br/> |Centres d’intérêt ou centres d’intérêt de la personne.  <br/> |
|**lastModificationTime** <br/> |Heure de dernière modification du profil de la personne sur le réseau social.  <br/> |
|**lastName** <br/> |Nom de famille de la personne.  <br/> |
|**location** <br/> |L’emplacement de la personne.  <br/> |
|**surnom** <br/> |Un nom plus court ou fantaisie nom de la personne.  <br/> |
|**otherAddress** <br/> |Autre adresse postale de la personne.  <br/> |
|**otherCity** <br/> |Ville de l’adresse secondaire de la personne.  <br/> |
|**otherCountryOrRegion** <br/> |Pays ou région de l’adresse secondaire de la personne.  <br/> |
|**otherState** <br/> |État ou province de l’adresse secondaire de la personne.  <br/> |
|**otherZip** <br/> |ZIP ou le code postal de l’adresse secondaire de la personne.  <br/> |
|**téléphone** <br/> |Numéro de téléphone du contact principal pour la personne.  <br/> |
|**URL de la photo** <br/> |URL d’une image de profil de la personne.  <br/> |
|**relation** <br/> |Relation de cette personne avec l’utilisateur connecté.  <br/> |
|**écoles** <br/> |Écoles que la personne atteint ou est passé à.  <br/> |
|**compétences** <br/> |Compétences personnelles de la personne.  <br/> |
|**state** <br/> |État ou province de l’adresse physique de la personne.  <br/> |
|**title** <br/> |Désignation ajoutée à nom son.  <br/> |
|**nom d’utilisateur** <br/> |ID pour identifier la personne sur le réseau social.  <br/> |
|**webProfilePage** <br/> |Adresse de page Web qui contient un profil de la personne.  <br/> |
|**site Web** <br/> |Site web de la personne.  <br/> |
|**workPhone** <br/> |Numéro de téléphone professionnel de la personne.  <br/> |
|**ZIP** <br/> |Code postal ou un code postal de l’adresse physique de la personne.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Exemple de code XML amis](friends-xml-example.md)  
- [Synchronisation de vos amis et activités](synchronizing-friends-and-activities.md)  
- [Fichier XML pour les fonctionnalités](xml-for-capabilities.md) 
- [XML pour les activités](xml-for-activities.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

