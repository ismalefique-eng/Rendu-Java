let personnage1 = {
    "nom" : "Hero",
    "pv" : 80,
    "attaque": 10,
    "precision": 0.8
}

let personnage2 = {
    "nom" : "Monster",
    "pv" : 60,
    "attaque": 20,
    "precision": 0.5
}

function attaquer(attaquant, victime){
    let attackPasse = precision(attaquant["precision"])
    if(attackPasse == false){
        console.log("ca touche pas")
        return victime["pv"]
    }
    console.log("ca touche")
    console.log(attaquant["nom"] + " a fait des dégats à " + victime["nom"])
    console.log("il reste " + (victime["pv"]-attaquant["attaque"]) + " à " + victime["nom"])
    return victime["pv"] - attaquant["attaque"]
}

const precision = (precisonCombatant) => {
    return Math.random() < precisonCombatant
}

while(personnage1["pv"]>0 && personnage2["pv"]>0){
    personnage2["pv"] = attaquer(personnage1, personnage2)
    if(personnage2["pv"] > 0){
        personnage1["pv"] = attaquer(personnage2,personnage1)
    }
}

if (personnage1["pv"] <= 0) {
    console.log("personnage2 a gagné");
} else {
    console.log("personnage1 a gagné");
}
