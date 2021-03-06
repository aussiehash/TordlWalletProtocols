# Basic Master Passphrase

## Variable Parameters

* `Devices` that the passphrase will be used on.
* `Frequency of Use` - eg "every day" vs "once or twice a month". 

## Steps

1. Choose a passphrase with 3-5 random words and a few numbers. It MUST be memorable to you but should NOT use words that are meaningful to you or associated with your identity, even things you think are secret. The more words it has, the more secure it is, however the harder it will be to remember. It is NOT recommended to use any punctuation, special characters, letter/number substitution, nor to use capitalization.
2. Do NOT record the password anywhere - store your password only in your head.
3. Do NOT use this password on any website or service that requires sending your password to another person or organization. It should never be sent over the internet and should only be used on devices you own.
4. Ideally, you should only have a small number (1-4) of important passwords like this. Any non-critical password you might need should be stored in an open-source password manager. See [Non-critical Password](Non-critical-Password.md) for details.
5. If you don't use this password often enough, set a calendar reminder to remind you to recite it in your head on a regular basis (say once per month).

Notes:

* The less often you use a passphrase, the more secure it is, because it's less likely someone will observe you entering it. It might make sense, for example, to have one master passphrase you use often (multiple times a day) that you use to protect commonly used things and another master passphrase you use sparingly (only once a month or a few times a year) for more important things used more rarely, like the seed for a cold wallet.
* The fewer physical locations you enter your password at and the fewer different devices you enter it on, the more secure it is. 
* The more secure the devices you enter your passphrase on are, the more secure your passphrase itself is. Because malware on a windows machine could easily spy on keyboard input or screen output, any password entered on a windows machine is less secure than a password entered only on a standard smart phone. Entering the master passphrase on a website is even worse (much worse, so again, don't do that). The weakest device you use your passphrase on is a significant factor for the security of your passphrase. The most secure extreme version of this is an [Offline Master Passphrase](Offline-Master-Passphrase.md).

## Rationale

A passphrase is intended to be the "something you know" in the [three factors of authentication](http://www.pearsonitcertification.com/articles/article.aspx?p=1718488).

1. 3-5 words and a few numbers is a sweet spot where the password is memorable but still hard to guess. A passphrase without numbers or with two or fewer words or [don't have enough entropy](https://protonmail.com/blog/protonmail-com-blog-password-vs-passphrase/) to be secure. More words are better than punctuation, special characters, etc, because they are harder to remember than an additional word and increase the security of the passphrase less than an additional word. As of 2019, a passphrase with 4 words should take about a year for a GPU to crack and a couple days for [a hypothetical future ASIC to crack](https://coldbit.com/can-bip-39-passphrase-be-cracked/). Add in just 1 number and that should increase that to at least 50 years for a GPU and half a year for the hypothetical ASIC.
2. It should not be recorded anywhere because that would turn it into "something you have" instead of "something you know".
3. Although this isn't an [Offline Master Passphrase](Offline-Master-Passphrase.md), a Basic Master Passphrase should have a limited exposure. Sending it over the internet gives other entities access to your password. Using it on a machine you don't own gives unknown entities control over your password.
4. Trying to remember many passwords makes it far more likely to forget some of those passwords.
5. You're likely to remember the passwords you use most often, while the most important passwords might be ones you use least often.

## Weaknesses

* Since a basic master password may be used on an online machine, it can be stolen by malware and transmitted to remote attackers.

## See also

* [Picking a Good 25th Word by Crypto Guide](https://www.youtube.com/watch?v=nhjq_1J0EbU&feature=youtu.be)
* [Realistic password strength estimation](https://blogs.dropbox.com/tech/2012/04/zxcvbn-realistic-password-strength-estimation/)

![xkcd password strength](https://imgs.xkcd.com/comics/password_strength.png)