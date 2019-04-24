---
title: Exemple de code XML sur les amis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83afbdef-4f12-4673-a0c1-bbf86274558f
description: "L'exemple XML de cette rubrique est une chaîne XML Friend renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode ISocialPerson:: GetFriendsAndColleagues. L'exemple montre le code XML Friends de deux amis, chacun étant délimité par l'élément person. Chaque ami spécifie une valeur unique pour l'élément userID sur le réseau social."
ms.openlocfilehash: 5dbda1e4439f807ccc6e7abddd0ef654ae801fe0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280958"
---
# <a name="friends-xml-example"></a><span data-ttu-id="aa5a3-105">Exemple de code XML sur les amis</span><span class="sxs-lookup"><span data-stu-id="aa5a3-105">Friends XML example</span></span>

<span data-ttu-id="aa5a3-106">L'exemple XML de cette rubrique est une chaîne XML Friend renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) .</span><span class="sxs-lookup"><span data-stu-id="aa5a3-106">The XML example in this topic is a friend XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method.</span></span> <span data-ttu-id="aa5a3-107">L'exemple montre le \*\*\*\* code XML Friends de deux amis, chacun étant délimité par l'élément **Person** .</span><span class="sxs-lookup"><span data-stu-id="aa5a3-107">The example shows the **friends** XML for two friends, each delimited by the **person** element.</span></span> <span data-ttu-id="aa5a3-108">Chaque ami spécifie une valeur unique pour l'élément **userid** sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="aa5a3-108">Each friend specifies a unique value for the **userID** element on the social network.</span></span> 
  
<span data-ttu-id="aa5a3-109">Les éléments restants \*\*\*\* du XML Friends ont des noms explicites.</span><span class="sxs-lookup"><span data-stu-id="aa5a3-109">The remaining elements of the **friends** XML have self-explanatory names.</span></span> <span data-ttu-id="aa5a3-110">Pour obtenir une description détaillée de ces éléments, consultez la rubrique [XML pour les amis](xml-for-friends.md).</span><span class="sxs-lookup"><span data-stu-id="aa5a3-110">For detailed description of these elements, see [XML for Friends](xml-for-friends.md).</span></span> 
  
## <a name="xml-example"></a><span data-ttu-id="aa5a3-111">Exemple XML</span><span class="sxs-lookup"><span data-stu-id="aa5a3-111">XML example</span></span>

<span data-ttu-id="aa5a3-112">L'exemple suivant montre les **amis** XML de deux personnes sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="aa5a3-112">The following example shows the **friends** XML for two persons on the social network.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<friends xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <person>
    <userID>4667647</userID>
    <firstName>Melissa</firstName>
    <lastName>MacBeth</lastName>
    <nickname></nickname>
    <fileAs>MacBeth, Melissa (Contoso Ltd.)</fileAs>
    <company>Contoso Ltd.</company>
    <title>Product Manager</title>
    <anniversary>2005-05-17</anniversary>
    <birthday>1979-08-09</birthday>
    <emailAddress>melissa@contoso.com</emailAddress>
    <emailAddress2>melissa@fabrikam.com</emailAddress2>
    <emailAddress3>melissa@adventureworks.com</emailAddress3>
    <webProfilePage>https://contoso.com/melissa</webProfilePage>
    <phone>800-555-1212</phone>
    <cell>888-555-1212</cell>
    <workPhone>425-555-1212</workPhone>
    <creationTime>2010-01-08T08:30:20-08:00</creationTime>
    <lastModificationTime>2010-01-08T11:40:14-08:00</lastModificationTime>
    <expirationTime>2010-01-09T11:40:14-08:00</expirationTime>
    <gender>female</gender>
    <index>0</index>
  </person>
  <person>
    <userID>5015012</userID>
    <firstName>Michael</firstName>
    <lastName>Affronti</lastName>
    <nickname>Mr. Social</nickname>
    <fileAs>Affronti, Michael (Contoso Ltd.)</fileAs>
    <company>Contoso Ltd.</company>
    <title>Sales Director</title>
    <anniversary>2009-06-21</anniversary>
    <birthday>1980-09-10</birthday>
    <emailAddress>michael@contoso.com</emailAddress>
    <emailAddress2>michael@fabrikam.com</emailAddress2>
    <emailAddress3>michael@adventureworks.com</emailAddress3>
    <webProfilePage>https://contoso.com/michael</webProfilePage>
    <phone>800-555-1212</phone>
    <cell>888-555-1212</cell>
    <workPhone>425-555-1212</workPhone>
    <creationTime>2010-01-08T08:30:20-08:00</creationTime>
    <lastModificationTime>2010-01-08T11:40:14-08:00</lastModificationTime>
    <expirationTime>2010-01-09T11:40:14-08:00</expirationTime>
    <gender>male</gender>
    <index>1</index>
  </person>
</friends>

```

## <a name="see-also"></a><span data-ttu-id="aa5a3-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa5a3-113">See also</span></span>

- [<span data-ttu-id="aa5a3-114">Exemples de fournisseurs XML OSC</span><span class="sxs-lookup"><span data-stu-id="aa5a3-114">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="aa5a3-115">Exemple de XML de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="aa5a3-115">Capabilities XML Example</span></span>](capabilities-xml-example.md) 
- [<span data-ttu-id="aa5a3-116">Exemple de XML d'informations sur les activités</span><span class="sxs-lookup"><span data-stu-id="aa5a3-116">Activity Feed XML Example</span></span>](activity-feed-xml-example.md) 
- [<span data-ttu-id="aa5a3-117">Schéma XML du fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="aa5a3-117">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

